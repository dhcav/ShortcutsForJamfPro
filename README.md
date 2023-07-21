# ShortcutsForJamfPro
A collection of Shortcuts for iOS, iPadOS, macOS and even sometimes watchOS to be used with Jamf Pro. 


## Notes
Repo is under construction. Follow or check back regularly for new Shortcuts!


### Shortcut Compatibility
- macOS 13 Ventura
- iOS/iPadOS 16

Unless otherwise noted, all Shortcuts will be fully self-contained and not run other Shortcuts or use third party apps. Where possible, they will be device-agnostic in using Actions that are present on all supported OSs (e.g. avoiding Mac-only Actions). 


### Security
Just want to clearly state that I'm not happy about having to encode Jamf Pro credentials in plain text. You could change this to ask for username/password each time it's run but that's a terrible user experience. 

Until there is a Jamf Shortcuts app to provide auth via approved Actions this is the simplest way. I have devised a system using the Data Jar app to store credentials and Jamf server info outside of the shortcut itself (which incidentally supports multiple servers and accounts under each) but this approach requires reasonably advanced Shortcuts knowledge so will be released sometime in future. 

***Unless you have customised one of my Shortcuts to your environment and are sharing within your team, I strongly suggest you share via this GitHub page to reduce the chance of inadvertantly sharing your Jamf API account's credentials!***


### Troubleshooting & Known Issues:
Shortcuts can at times be a capricious little beast, so if encountering an issue try quitting and reopening tha app, and restarting if it persists. Aside from that:
- Ensure you have populated your credentials in the correct fields. I attempt to use the 'Import Questions' feature to request this on first installing the Shortcut but know this doesn't always happen
- Jamf Pro user accounts using federated auth (e.g. Azure AD) are not currently supported. Working on this currently as this may faciliate a better approach to security


### Feedback
We're essentially in the pre-history of Shortcuts being used for Mac Admin workflows. As such, please feed back any issues that you encounter with these Shortcuts as issues or via the Mac Admins Slack (I'm d.cav).

I am particularly keen on feedback on:
- Input methods to support. This all began with a QR code of the device's serial but have since expanded to using the Jamf Pro Mac invoentory page's URL, clipboard, using Asset Tags instead of serials in the QR. I am currently working on being able to use a CSV in order to get MUT-like capabilities. Ideas of this type greatly appreciated
- More efficient API calls. I am self-taught and constantly learning newer, better ways of doing things - both with Shrotcuts and APIs. As I get around to uploading all my shortcuts, you may notice a increase in sophistication from when I started a few years ago to now. If you have experience with RESTful APIs and notice any quick wins, or even basic errors, please let me know

