# iOS development tips
Misc tips for iOS development
- Xcode
- Debugging
- UI Testing

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
