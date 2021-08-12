
iOS
============

Developing apps for Apple's mobile platform
--------------------------

### What is iOS?
iOS is a mobile operating system used on iPhones, thus the second most popular mobile OS following Android. It is a very popular platform to build and develop apps. iPhone applications are written in Objective C or Swift, but Swift is more intuitive for beginners and like its name, Swift is designed to be swift. You can learn more about Swift programming with the official documentation [here](https://swift.org/documentation).

Xcode is the official development tool designed by Apple. As Xcode is only a Mac App, it requires developers to possess a macOS running machine. You will also need a developer account by enrolling your Apple ID in the Apple Developer Program [here](https://idmsa.apple.com/IDMSWebAuth/signin?appIdKey=891bd3417a7776362562d2197f89480a8547b108fd934911bcbea0110d07f757&path=%2Faccount%2F&rv=1) or at [developer.apple.com/](developer.apple.com/). You can download Xcode 12 from App Store, create a new Xcode project, choose from the preset application modules, and take time to explore the File Navigator, Code Editor, Interface Builder, Inspector Panel, and more. Apple has developed a great [Xcode documentation guide](https://developer.apple.com/documentation/xcode) if you encounter any problem during your development.

### Planning
First step of app development is to determine the presentation, data collected, and the user interaction of the app. A common practice is design wireframe/mockups on the app either on paper or with applications (Great for collaboration). Though they might seem repetitive, app mockups provide a great visual aid to focus on improving user experience without distractions from the complex logics. Some popular applications include Figma (Free web version) and Adobe Software (XD or Illustrator on paid plans).

### Development
Xcode utilizes the Model, View, Control (MVC) framework to separate data (Model), user interface (View), and application logic (Controller). The model layer contains all your app’s data including network code, parsing code, helpers, constants, and etc. The view layer contains all the graphic components, and the controller layer controls all the logic that updates between model and view.
[SwiftUI](https://developer.apple.com/documentation/swiftui/), since Xcode 11, allows users to build declarative UI.  Compare to [UIKit](https://developer.apple.com/documentation/uikit), an imperative user interface builder where you have to implement every action, SwiftUI handles under the hood implementation from your declaration in the swift code. Watch this [WWDC video](https://developer.apple.com/videos/play/wwdc2019/216/) to compare imperative and declarative UI.

### Test
With the free developer’s account, you can build and run the app on your iOS device. If you signed up for the paid developer plan, you can use TestFlight to push your latest development for over-the-air installation and testing.
If you want your app to interface with different operating systems (Android and iOS), you don’t have to start from scratch. There are a variety of third-party SDKs for native app development. Flutter is one of the most popular platforms developed by Google that you can deploy to Xcode and Android Studio. Take a look at the documentation [here](https://flutter.dev/docs/get-started/flutter-for/ios-devs).

### Resources

[Apple documentation](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html)

[Apple Developer's Road Map to iOS](https://developer.apple.com/library/iOS/referencelibrary/GettingStarted/RoadMapiOS/index.html)

[XCode IDE](https://developer.apple.com/xcode/)

[iOS development lab](http://www.hongkiat.com/blog/ios-development-guide-part1/)

[iOS App Dev Tutorial by Apple](https://developer.apple.com/tutorials/app-dev-training/)

[iOS App Dev Tutorial](https://raywenderlich.com/ios/)
