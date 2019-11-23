# Real time Swift iOS Chat with Firebase - Messenger Clone

This is an extremely simple chat app source code of an iOS Swift Chat app. It leverages <a href="https://github.com/MessageKit/MessageKit">MessageKit</a> and it stores and retrieves data to/from Firebase Firestore. The app design is inspired by Facebook Messenger. Clone the iOS Chat App Source Code and add a fully fledged chat to your app in minutes.

## App Designs

<div align="center">
    <img src="https://github.com/samyka/iOS-chat-app/blob/master/SreenShot/os-chat-app.png" width="600px"</img>
</div>

<b> This project has now been updated to Swift 5. Make sure you run Xcode's Legacy Build System (File -> Workspace Settings).</b>

## How to run a demo app

1. Download the source code by cloning this repository
2. Download the GoogleService-Info.plist file from your <a href="https://console.firebase.google.com">Firebase Console</a> and replace the existing file in ChatApp folder. This will connect the app to your own Firebase instance.
3. Install the pods by running

```
pod update
```

4. Open the xcworkspace file with the latest version of Xcode

## How to integrate the chat into your app

1. Download the source code and import the "Core" folder into your Xcode project
2. Make sure you add all the Podfile dependencies into your own Podfile
3. Replace the GoogleService-Info.plist file with your own file, downloaded from Firebase Console.
4. Install the pods

```
pod update
```

5. Use the following code to instantiate a chat view controller

```swift
let uiConfig = ATCChatUIConfiguration(primaryColor: UIColor(hexString: "#0084ff"),
                                      secondaryColor: UIColor(hexString: "#f0f0f0"),
                                      inputTextViewBgColor: UIColor(hexString: "#f4f4f6"),
                                      inputTextViewTextColor: .black,
                                      inputPlaceholderTextColor: UIColor(hexString: "#979797"))
let channel = ATCChatChannel(id: "channel_id", name: "Chat Title")
let viewer = ATCUser(firstName: "Florian", lastName: "Marcu")
let chatVC = ATCChatThreadViewController(user: viewer, channel: channel, uiConfig: uiConfig)

// Present the chatVC view controller

```

6. Customize the UI by updating the ChatUIConfiguration class

```swift
    let mainThemeBackgroundColor: UIColor = .white
    let mainThemeForegroundColor: UIColor = UIColor(hexString: "#3068CC")
    let mainTextColor: UIColor = UIColor(hexString: "#000000")
    let mainSubtextColor: UIColor = UIColor(hexString: "#7e7e7e")
    let statusBarStyle: UIStatusBarStyle = .default
    let hairlineColor: UIColor = UIColor(hexString: "#d6d6d6")

    let regularSmallFont = UIFont.systemFont(ofSize: 14)
    let regularMediumFont = UIFont.systemFont(ofSize: 17)
    let regularLargeFont = UIFont.systemFont(ofSize: 23)
    let mediumBoldFont = UIFont.boldSystemFont(ofSize: 17)
    let boldLargeFont = UIFont.boldSystemFont(ofSize: 23)
    let boldSmallFont = UIFont.boldSystemFont(ofSize: 14)
    let boldSuperSmallFont = UIFont.boldSystemFont(ofSize: 11)
    let boldSuperLargeFont = UIFont.boldSystemFont(ofSize: 29)

    let italicMediumFont = UIFont.italicSystemFont(ofSize: 17)
```

This project was created using <a href="https://www.cupertinokit.com/">Cupertino Kit</a>.
# iOS-chat-app
