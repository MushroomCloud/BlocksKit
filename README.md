This fork removes all references to UIImagePickerController, so that the app won't get rejected by Apple when submitting with Xcode 8 because of a missing `NSPhotoLibraryUsageDescription` key in the info.plist.

It also removes the additions to `UIWebView`, which has been deprecated.

[BlocksKit](https://zwaldowski.github.io/BlocksKit)
===================================================

Blocks in C and Objective-C are downright magical.  They make coding easier and potentially quicker, not to mention faster on the front end with multithreading and Grand Central Dispatch.  BlocksKit hopes to facilitate this kind of programming by removing some of the annoying - and, in some cases, impeding - limits on coding with blocks.

BlocksKit is a framework for OS X Mountain Lion and newer, a static library for iOS 6 and iOS 7, and a framework for iOS 8 and newer.

BlocksKit was created by [Zachary Waldowski](https://github.com/zwaldowski) and [Alexsander Akers](https://github.com/a2) and is maintained by the former.

Installation
============

BlocksKit can be added to a project using [CocoaPods](https://github.com/cocoapods/cocoapods). One may also use targets included in the project.

### Framework

* Download a release of BlocksKit.
* Drag (or "Add Files...") `BlocksKit.xcodeproj` to *your* Xcode project using
the Navigator.
* From the "General" pane of your application or framework, add
`BlocksKit.framework` to the "Embedded Binaries" list.
* `@import BlocksKit;`

### Static Library

* Download a release of BlocksKit.
* Run "Archive" in Xcode.
* By default the static library will be compiled to `~/Library/Developer/Xcode/DerivedData`.
* Move libBlocksKit.a and Headers to your project's folder, preferably a subfolder like "Vendor".
* In "Build Phases", Drag libBlocksKit.a into your target's "Link Binary With Libraries" build phase.
* In the build settings of your target or project, change "Other Linker Flags" to `-ObjC`. Make sure your app is linked with CoreGraphics, Foundation, MessageUI, and UIKit.
* Change (or add) to "Header Search Paths" the relative path to BlocksKit's headers, like `$(SRCROOT)/Vendor/Headers`.
* Insert `#import <BlocksKit/BlocksKit.h>` in your project's prefix header.

Documentation
=============

An Xcode-compatible documentation set is available [from CocoaDocs](http://cocoadocs.org/docsets/BlocksKit/).

License
=======

BlocksKit is maintained under the MIT license.  **The project itself is free for use in any and all projects.**  You can use BlocksKit in any project, public or private, with or without attribution - though we prefer attribution! It helps us.

Unsure about your rights?  [Read more.](http://opensource.org/licenses/MIT)

Individual credits for included code exist in the header files and documentation. We thank them for their contributions to the open source community.

Documentation help has been contributed by [Alex Gray](https://github.com/mralexgray).

