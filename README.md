# iOS development tips
Misc tips for iOS development
- [Swift](https://github.com/nigarcia88/ios_tips#swift)
- [Xcode](https://github.com/nigarcia88/ios_tips#xcode)
- [Debugging](https://github.com/nigarcia88/ios_tips#debugging)
- [UI Testing](https://github.com/nigarcia88/ios_tips#ui-testing)
- [App Store](https://github.com/nigarcia88/ios_tips#app-store)
- [In-app purchases](https://github.com/nigarcia88/ios_tips#in-app-purchases)
- [Apple](https://github.com/nigarcia88/ios_tips#apple)

## Swift

### The Official raywenderlich.com Swift Style Guide
- [Source](https://github.com/raywenderlich/swift-style-guide)

### Learning sources
- [Objc.io](https://www.objc.io/)
- [Ray Wenderlich](https://www.raywenderlich.com/)
- [Swift by Sundell](https://www.swiftbysundell.com/)

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
- [Five In-App Purchase Mistakes to Avoid](https://cocoacasts.com/five-in-app-purchase-mistakes-to-avoid)
- [Best practices Technical Note TN2387](https://developer.apple.com/library/content/technotes/tn2387/_index.html#//apple_ref/doc/uid/DTS40014795-CH1-BEST_PRACTICES-TEST_YOUR_IMPLEMENTATION_OF_IN_APP_PURCHASE)
- [FAQ Technical Note TN2413](https://developer.apple.com/library/content/technotes/tn2413/_index.html)
- [In-App Purchase Debugging Lessons](http://www.mokacoding.com/blog/in-app-purchase-debugging-lessons/)

## Apple
- [System status](https://www.apple.com/support/systemstatus/)
