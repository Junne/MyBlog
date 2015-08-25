title: "Swift"
date: 2015-08-25 13:39:50
tags: [iOS,Swift]
---


Swift已然成为苹果主力推动的语言，OC虽然在一定时间内还有其存在并使用的价值，但从[Ray](http://www.raywenderlich.com)的教程来看，满屏的Swift就会让你觉得是时候使它成为你的生产力工具了 :)  

<h3 id="1">Start</h3>
学习一门语言最快的就是去运用，做一个小的应用，不会的再去查资料，再做之前看一些Github上优秀的源码也是有必要的,例如可以先看看这些: [HackerNews](https://github.com/amitburst/HackerNews) [DesignerNewsApp](https://github.com/MengTo/DesignerNewsApp) 当你遇到有些基础知识不会的时候可以看看这些参考书:[The Swift Programming Language 中文版](http://wiki.jikexueyuan.com/project/swift/) 苹果关于Siwft资源的[主页](https://developer.apple.com/swift/resources/) 列举了很多资源，包括斯坦福的CS193p、书、WWDC视频、例子源码，都是不错的学习资源.  

<h3 id="2">CocoaPods VS Carthage</h3>
当你真正开始开发项目的时候，也许你会使用很多第三方库，这个时候你要选择一个好的第三库管理工具，这个时候你也许会在[CocoaPods](https://github.com/CocoaPods/CocoaPods)和[Carthage](https://github.com/Carthage/Carthage)之间做出一些选择，那该怎样选择呢？可以看看[这篇文章](http://imtx.me/archives/1939.html)  
CocoaPods的使用我想大家都非常熟悉 :)   
创建Podfile文件:  

```
pod init
```

打开Podfile文件后添加你需要的库:


```
platform :ios, '8.0'
use_frameworks!

target 'Weather' do
pod 'Alamofire', '~>1.3'
pod 'SwiftyJSON', '~>2.2.1'
end

target 'WeatherTests' do

end
```

继而安装一下就能使用了:  

```
pod install
```


Carthage使用起来也相当简单:  
首先创建一个名为Cartfile的文件，然后列出你想使用的库地址，例如:  

```
github "Alamofire/Alamofire"
github "SwiftyJSON/SwiftyJSON"
```

然后安装一些就OK了:  

```
carthage update
```

<h3 id="3">Alamofire</h3>
[Alamofire](https://github.com/Alamofire/Alamofire)无疑是Siwft版的AFNetworking.使用起来也相当方便，可以先看看这个[教程](http://www.raywenderlich.com/85080/beginning-alamofire-tutorial) 还有这个[封装的库](https://github.com/Moya/Moya)  