title: "动态UITableViewCell的高度计算"
date: 2015-06-18 13:47:43
tags: iOS
---
iOS开发中经常会遇到不同cell因为字体图片大小等的原因从而高度有多不同，这个时候就需要我们动态的计算cell的高度了，那么如何来进行计算呢？  

<h3 id="1">iOS 8</h3>
你可以在[这篇文章](http://www.raywenderlich.com/87975/dynamic-table-view-cell-height-ios-8-swift)学习下iOS中利用Autolayout来动态计算高度，步骤大概为:  

> 1.利用AutoLayout 创建tableview的cell内容  
> 2.设置cell的rowHeight=UITableViewAutomaticDimension  
> 3.设置estimatedRowHeight或者实现height estimation的代理方法  


在设置Autolayout时有时会遇到下图中的设置：  
![HorizontalVertical](http://7xjmzg.com1.z0.glb.clouddn.com/HorizontalVertical.png)  
这是设置压缩和放大的优先级，可以参考[这篇文章](http://blog.csdn.net/yongyinmg/article/details/39526207)  
如果你对AutoLayout还不太熟，可以做个[小练习](http://www.raywenderlich.com/83129/beginning-auto-layout-tutorial-swift-part-1)    


```
tableView.rowHeight = UITableViewAutomaticDimension  
tableView.estimatedRowHeight = 80.0 
```

或者实现estimatedHeightForRowAtIndex的代码方法: 

  
```
func tableView(tableView: UITableView, estimatedHeightForRowAtIndexPath indexPath: NSIndexPath) -> CGFloat {
  if isLandscapeOrientation() {
    return hasImageAtIndexPath(indexPath) ? 140.0 : 120.0
  } else {
    return hasImageAtIndexPath(indexPath) ? 235.0 : 155.0
  }
} 
```
 
其中estimatedRowHeight是根据你项目需要设置的高度,超简单吧,再也不用计算不同字体UILabel等的大小高度了:)  
 
<h3 id="2">iOS 7</h3>

可以先看看[这篇文章](http://www.raywenderlich.com/73602/dynamic-table-view-cell-height-auto-layout)  
关键要实现heightForRowAtIndexPath这个代理方法:  


```  

- (CGFloat)tableView:(UITableView *)tableView heightForRowAtIndexPath:(NSIndexPath *)indexPath {
  return [self heightForBasicCellAtIndexPath:indexPath];
}
 
- (CGFloat)heightForBasicCellAtIndexPath:(NSIndexPath *)indexPath {
  static RWBasicCell *sizingCell = nil;
  static dispatch_once_t onceToken;
  dispatch_once(&onceToken, ^{
    sizingCell = [self.tableView dequeueReusableCellWithIdentifier:RWBasicCellIdentifier];
  });
 
  [self configureBasicCell:sizingCell atIndexPath:indexPath];
  return [self calculateHeightForConfiguredSizingCell:sizingCell];
}
 
- (CGFloat)calculateHeightForConfiguredSizingCell:(UITableViewCell *)sizingCell {
  [sizingCell setNeedsLayout];
  [sizingCell layoutIfNeeded];
 
  CGSize size = [sizingCell.contentView systemLayoutSizeFittingSize:UILayoutFittingCompressedSize];
  return size.height + 1.0f; // Add 1.0f for the cell separator height
} 

```  
 

这就需要计算cell中contentView的高度，一般根据字数多少和字的大小来计算。  

<h3 id="3">Resource</h3>
* [UITableView Tutorial:Dynamic Table View Cell Height](http://www.raywenderlich.com/87975/dynamic-table-view-cell-height-ios-8-swift)  
* [UITableView-FDTemplateLayoutCell:for automatically UITableViewCell height calculating](https://github.com/forkingdog/UITableView-FDTemplateLayoutCell)
* [Dynamic Table View Cell Height and Auto Layout](http://www.raywenderlich.com/73602/dynamic-table-view-cell-height-auto-layout)  
* [Auto Layout Guide](https://developer.apple.com/library/prerelease/ios/documentation/UserExperience/Conceptual/AutolayoutPG/Introduction/Introduction.html)  
