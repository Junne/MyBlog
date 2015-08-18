title: "Glance at Watch OS 2"
date: 2015-06-14 22:28:08
tags: [watchOS,iOS] 
---

![watchos2](http://7xjmzg.com1.z0.glb.clouddn.com/watchos2.png)

<h3 id="1">Architecture</h3>
WatchOS 2 can run the WatchKit extension on the user's Apple Watch and make it possible for your app to run when your phone is not present.We have a look from the pic below:  
![watchos2architecture](http://7xjmzg.com1.z0.glb.clouddn.com/watchos2architecture.png)
WatchOS 1: Apple Watch requires the presence of an iPhone to run third-party apps. To create a third-party app, you need two separate bundles: a WatchKit app (that runs on Apple Watch) and a WatchKit extension (that runs on the user’s iPhone). The WatchKit app contains only the storyboards and resource files associated with your app’s user interface. The WatchKit extension contains the code for managing the WatchKit app’s user interface and for responding to user interactions.(from[Apple Watch Programming Guide](https://developer.apple.com/library/ios/documentation/General/Conceptual/WatchKitProgrammingGuide/index.html#//apple_ref/doc/uid/TP40014969))  
<h3 id="2">Glance</h3>
Glance displays timely and relevant information from your app.It's a read-only interface.A glance is a focused interface that you use to display your app’s most important information. Glances are aptly named because they are intended to be looked at quickly by the user. Glances are nonscrolling; the entire glance interface must fit on a single screen. Glances are read-only and cannot contain buttons, switches, or other interactive controls. Tapping a glance launches your WatchKit app.  
<h3 id="3">Lifecycle</h3>
Launching a WatchKit app:  
![watchoslifecycle](http://7xjmzg.com1.z0.glb.clouddn.com/watchoslifecycle.png)
The life cycle of an interface controller:  
![interfacelifecycle](http://7xjmzg.com1.z0.glb.clouddn.com/interfacelifecycle.png)
<h3 id="4">Resource</h3>
* [Apple Watch Programming Guide](https://developer.apple.com/library/ios/documentation/General/Conceptual/WatchKitProgrammingGuide/index.html#//apple_ref/doc/uid/TP40014969)  
* [WatchKit Programming Guide](https://developer.apple.com/library/prerelease/watchos/documentation/General/Conceptual/WatchKitProgrammingGuide/)  
* [watchOS 2 Transition Guide](https://developer.apple.com/library/prerelease/watchos/documentation/General/Conceptual/WatchKitProgrammingGuide/)  
* [Apple Watch Human Interface Guidelines](https://developer.apple.com/watch/human-interface-guidelines/)  
* [WatchKit Development Tips and Best Practices](https://developer.apple.com/watchkit/tips/)  
* [Raywenderlich Watch Tutorial](http://www.raywenderlich.com/?s=watchkit&cof=FORID%3A10)  
* [Session 105:Introducing WatchKit for watchOS 2](https://developer.apple.com/videos/wwdc/2015/?id=105)  
* [Session 207:WatchKit In-Depth,Part 1](https://developer.apple.com/videos/wwdc/2015/?id=207)  
* [Session 208:WatchKit In-Depth,Part 2](https://developer.apple.com/videos/wwdc/2015/?id=208)  
* [Session 207&208 Note](https://www.icloud.com/pages/AwBWCAESEC9BxhCXUuOOg6ChrE-uZrwaKmQPtEHrcL7HFI4JgHygl08BETTFumet_i93LbIsRno9Gd3BFuo_APnDrQMCUCAQEEIIvE_BC86PVjR4kOIrboTvPUlOydWDyujn1yUU59Mv_S#WWDC15_Session_207,_208_WatchKit_In-Depth)  


