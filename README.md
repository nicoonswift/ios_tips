# iOS development tips
Misc tips for iOS development
* [Best Practices](#best-practices)
* [Swift](#swift)
* [Xcode](#xcode)
* [Debugging](#debugging)
* [UI Testing](#ui-testing)
* [App Store](#app-store)
* [In-app purchases](#in-app-purchases)
* [Apple](#apple)
* [Fastlane](#fastlane)
* [CocoaPods](#cocoapods)
* [To Read](#to-read)

## Best Practices

* [iOS-Factor](https://ios-factor.com): A methodology for building high-quality iOS apps on a solid architecture
* [Microfeatures Guidelines](https://github.com/xcode-project-manager/microfeatures-guidelines)

## Swift

### The Official raywenderlich.com Swift Style Guide
* [Source](https://github.com/raywenderlich/swift-style-guide)

### Learning sources
* [Objc.io](https://www.objc.io/)
* [Ray Wenderlich](https://www.raywenderlich.com/)
* [Swift by Sundell](https://www.swiftbysundell.com/)
* [Ole Begemann](https://oleb.net)

## Xcode

### Free HD space used by Xcode's derived data.
* Xcode 9.4.1
* Open terminal
* cd ~/Library/Developer/Xcode
* rm -rf DerivedData
* [Source](https://twitter.com/johnsundell/status/982274922528563200)

### Xcode 9.3 dev accounts session expiring on each app launch
* Open Terminal
* defaults write com.apple.dt.Xcode DVTDeveloperAccountUseKeychainService -bool NO
* [Source](https://stackoverflow.com/questions/49675844/xcode-9-3-session-expires-every-time-i-close-and-re-open-xcode)

### Easy-open project/workspace
* Open terminal
* cd ~
* xed .
* [Source](https://twitter.com/mluisbrown/status/1013205101933146113?s=12)

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">TIL: “xed .” will open the Xcode workspace or project file in the current directory. So many hours wasted typing “open projectname.xcworkspace” 🤦‍♂️ <a href="https://twitter.com/hashtag/swiftlang?src=hash&amp;ref_src=twsrc%5Etfw">#swiftlang</a></p>&mdash; Michael Luís Brown (@mluisbrown) <a href="https://twitter.com/mluisbrown/status/1013205101933146113?ref_src=twsrc%5Etfw">June 30, 2018</a></blockquote> 


## Debugging

### Dotzu, In-app logging tool
* Swift and Objective-C compatible
* Install through Cocoapods
* [Source](https://github.com/remirobert/Dotzu)

## UI Testing

### Doubling localized Strings
* Use NSDoubleLocalizedString as a launch argument
* [Source](https://twitter.com/JordanMorgan10/status/976611947767521285)

## Force Toggle Hardware Keyboard false (iOS Simulator)

* Xcode 9.4.1
* iOS 11.4.1
* [Source](https://stackoverflow.com/questions/38010494/is-it-possible-to-toggle-software-keyboard-via-the-code-in-ui-test) 

Add a _run script_ on UI Tests target:

```
/usr/libexec/PlistBuddy -c "Print :DevicePreferences" ~/Library/Preferences/com.apple.iphonesimulator.plist | perl -lne 'print $1 if /^    (\S*) =/' | while read -r a; do /usr/libexec/PlistBuddy -c "Set :DevicePreferences:$a:ConnectHardwareKeyboard
false" ~/Library/Preferences/com.apple.iphonesimulator.plist || /usr/libexec/PlistBuddy -c  "Add :DevicePreferences:$a:ConnectHardwareKeyboard
bool false" ~/Library/Preferences/com.apple.iphonesimulator.plist; done
```

### Using Localized Strings
* [Source](https://www.pixeldock.com/blog/how-to-use-your-localizable-strings-in-your-xcode-uitests/)

## App Store
* Guidelines
* [Source](https://developer.apple.com/app-store/guidelines/)

## In-app purchases
* [Testing Auto-Renewable Subscriptions on iOS](http://davidbarnard.com/post/164337147440/testing-auto-renewable-subscriptions-on-ios)
* [How to Set Up and Test an Auto-Renewable Subscription for an iOS App](https://savvyapps.com/blog/how-setup-test-auto-renewable-subscription-ios-app)
* [Five In-App Purchase Mistakes to Avoid](https://cocoacasts.com/five-in-app-purchase-mistakes-to-avoid)
* [Best practices Technical Note TN2387](https://developer.apple.com/library/content/technotes/tn2387/_index.html#//apple_ref/doc/uid/DTS40014795-CH1-BEST_PRACTICES-TEST_YOUR_IMPLEMENTATION_OF_IN_APP_PURCHASE)
* [FAQ Technical Note TN2413](https://developer.apple.com/library/content/technotes/tn2413/_index.html)
* [In-App Purchase Debugging Lessons](http://www.mokacoding.com/blog/in-app-purchase-debugging-lessons/)
* [What to do if In-App Purchases stop working?](https://kemenaran.winosx.com/posts/ios-developer-what-to-do-if-in-app-purchases-stop-working/)
* [The Definitive Guide to In-App Purchases Using Swift](https://www.airpair.com/ios/posts/swift-storekit-in-app-purchases)
* [What should the app do in response to a deferred SKPaymentTransaction?](https://stackoverflow.com/questions/26187148/what-should-the-app-do-in-response-to-a-deferred-skpaymenttransaction/26371545#26371545)
* [App Store Receipt Validation](https://github.com/IdeasOnCanvas/AppReceiptValidator)

## Apple
* [System status](https://www.apple.com/support/systemstatus/)

## Fastlane

* [Version Control with AVG](https://developer.apple.com/library/archive/qa/qa1827/_index.html)
* bundle exec fastlane beta
* If you want to skip waiting for the processing to be finished, use the `skip_waiting_for_build_processing` option
* [Unable to locate Xcode. Please make sure to have Xcode installed on your machine](https://github.com/fastlane/fastlane/issues/12263#issuecomment-379959724)

## Updating Ruby on macOS

### WARNING: You are running Ruby 2.3.7, which is nearing end-of-life.

The Google Cloud API clients work best on supported versions of Ruby. Consider upgrading to Ruby 2.4 or later.
See https://www.ruby-lang.org/en/downloads/branches/ for more info on the Ruby maintenance schedule.
To suppress this message, set the GOOGLE_CLOUD_SUPPRESS_RUBY_WARNINGS environment variable.

Proceed with:

* https://medium.com/@IanRahman/how-to-upgrade-ruby-on-a-mac-a592c6085c63
* https://github.com/rvm/rvm/issues/4215
* https://rvm.io/rvm/security

### Could not find CFPropertyList-3.0.0 in any of the sources

Your bundle is locked to json (1.8.3.1), but that version could not be found in
any of the sources listed in your Gemfile. If you haven't changed sources, that
means the author of json (1.8.3.1) has removed it. You'll need to update your
bundle to a version other than json (1.8.3.1) that hasn't been removed in order
to install.

Proceed with:
```
$ bundle update
```

[Source](https://github.com/bundler/bundler/issues/4462)

## CocoaPods

Execute the following on your terminal to get the latest stable version:

```
$ sudo gem install cocoapods
```

Add --pre to get the latest pre release:

```
$ sudo gem install cocoapods --pre
```

You can check pod version using below command

```
$ pod --version
```

### Tips

* https://www.cocoanetics.com/2014/07/development-pods/
* https://blog.takescoop.com/improve-ios-ci-build-time-with-cocoapods-caching-4a049ee45e63

### Pod Spec file validation

```
$ pod spec lint
```

For local development Pods

```
$ pod lib lint
```

# To Read

* http://www.joshholtz.com/altconf-fastlane-best-practices/
* https://medium.com/engineering-at-tink/buildkite-fastlane-the-key-to-better-sleep-for-ios-developers-2d01f429f95c



