![License](https://img.shields.io/badge/license-mit-black.svg?style=flat)
![Platform](https://img.shields.io/badge/platform-ios-lightgray.svg?style=flat)

# Swift ImageSlideShow for iOS
ImageSlideShow is a simple Slideshow for images (Picture, Photos) for your apps written in Swift 2.3.

![alt tag](https://raw.githubusercontent.com/dimix/ImageSlideShow/e6e9a62db2b4c82b58d5b298ef6802c0a8125970/demo.gif)

## Features
- All in one slideshow with generic protocol to provide images directly from the model
- Pan-gesture-to-dismiss behaviour (like Facebook)

## How to Use

#### 1. Import ImageSlideShow folder in your project
#### 2. Instantiate the controller

```swift
ImageSlideShowViewController.presentFrom(self){ [weak self] controller in
			
	controller.dismissOnPanGesture = true
	controller.slides = self?.images
	controller.enableZoom = true
	controller.controllerDidDismiss = {
		print("Controller Dismissed")
	}
			
}
```

You need to provide an array of `[ImageSlideShowProtocol]` objects.
You can use the Demo project to watch details.

## To Do

- Create module
- Add CocoaPods and Carthage support
- Create a Swift 3 version
