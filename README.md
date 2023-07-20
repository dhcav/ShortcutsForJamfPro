# ShortcutsForJamfPro
A collection of Shortcuts for iOS, iPadOS and macOS to be used with Jamf Pro. 

## Notes
Repo is under construction. Follow or check back regularly for new Shortcuts!

### Shortcut Compatibility
- macOS 13 Ventura
- iOS/iPadOS 16
Unless otherwise noted, all Shortcuts will be fully self-contained and not run other Shortcuts or use third party apps. Where possible, they will be device-agnostic in using Actions that are present on all supported OSs (e.g. avoiding Mac-only Actions). 

### Security
Just want to clearly state that I'm not happy about having to encode Jamf Pro credentials in plain text. You could change this to ask for username/password each time it's run but that's a terrible user experience. 

Until there is a Jamf Shortcuts app to provide auth via approved Actions this is the simplest way. I have devised a system using the Data Jar app to store credentials and Jamf server info outside of the shortcut itself (which incidentally supports multiple servers and accounts under each) but this approach requires reasonably advanced Shortcuts knowledge so will be released sometime in future. 

###
