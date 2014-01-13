SPMZoomableUIImageView
======================

This is a UIViewController that holds a `UIScrollView`. The scroll view holds a `UIImageView` with a `UIImage` which is zoomable. Pinch/Tap to zoom an image. Works with auto layout and rotation too.

## Zoomable Image View
It is recommeneded in the Apple Documentation that Zoomable/Pinch to Zoom functionality should be setup with a `UIScrollView` and `UIImageView`. 
Source - https://developer.apple.com/library/ios/documentation/windowsviews/conceptual/UIScrollView_pg/ZoomZoom/ZoomZoom.html

This example project shows how to implement this. A tutorial of how to accomplish this can also be [found here](http://www.raywenderlich.com/10518/how-to-use-uiscrollview-to-scroll-and-zoom-content).

###IOS7 Note
For IOS7 you should look to implement the following for status bar issues.
```if ([self respondsToSelector:@selector(automaticallyAdjustsScrollViewInsets)]) {
self.automaticallyAdjustsScrollViewInsets = NO;
}```

###Content Mode Fix (auto layout)
This project is set out to use Auto Layout as well. When the orientaion is changed the scrollView frame will automatically readjust itself. The issue with this is that the contentSize of the `UIScrollView` is changed to the frame and breaks the layout. To fix this we ammend the contentSize to the correct image size in the `-(void)didRotateFromInterfaceOrientation:(UIInterfaceOrientation)fromInterfaceOrientation `
[AutoLayout information](https://developer.apple.com/library/ios/technotes/tn2154/_index.html)

Please submit a pull request for any additional features

