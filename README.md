# iOS development tips
Misc tips for iOS development
- [Swift](https://github.com/nigarcia88/ios_tips#swift)
- [Xcode](https://github.com/nigarcia88/ios_tips#xcode)
- [Debugging](https://github.com/nigarcia88/ios_tips#debugging)
- [UI Testing](https://github.com/nigarcia88/ios_tips#ui-testing)
- [App Store](https://github.com/nigarcia88/ios_tips#app-store)

## Swift

### The Official raywenderlich.com Swift Style Guide
- [Source](https://github.com/raywenderlich/swift-style-guide)

## Xcode

### Free HD space used by Xcode's derived data.
- Open terminal
- cd ~/Library/Developer/Xcode
- rm -rf DerivedData
- [Source](https://twitter.com/johnsundell/status/982274922528563200)

### Xcode 9.3 dev accounts session expiring on each app launch
- Open Terminal
- defaults write com.apple.dt.Xcode DVTDeveloperAccountUseKeychainService -bool NO
- [Source](https://stackoverflow.com/questions/49675844/xcode-9-3-session-expires-every-time-i-close-and-re-open-xcode)

## Debugging

### Dotzu, In-app logging tool
- Swift and Objective-C compatible
- Install through Cocoapods
- [Source](https://github.com/remirobert/Dotzu)

## UI Testing

### Doubling localized Strings
- Use NSDoubleLocalizedString as a launch argument
- [Source](https://twitter.com/JordanMorgan10/status/976611947767521285)

## App Store
- Guidelines
- [Source](https://developer.apple.com/app-store/guidelines/)

## In-app purchases
- [Testing Auto-Renewable Subscriptions on iOS](http://davidbarnard.com/post/164337147440/testing-auto-renewable-subscriptions-on-ios)
- [How to Set Up and Test an Auto-Renewable Subscription for an iOS App](https://savvyapps.com/blog/how-setup-test-auto-renewable-subscription-ios-app)
