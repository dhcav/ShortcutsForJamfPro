# shortcutVersioner

*Created by Damian Cavanagh in August 2023*

*WORK IN PROGRESS*

This helper Shortcut checks the currentVersion of a parent Shortcut (from which it is run like a function using the Run Shortcut action) against the latest version on GitHub. 

If a newer version is available, the user receives a prompt with the new version number, their current version number, and release notes (retrieved along with the latest version from GitHub), and presented with an option to obtain the new version from GitHub or ignore and continue. 


### Inputs
Each Shortcut will feature a small dictionary holding:
- shortcutName
- currentVersion
- jamfProUrl

This Shortcut uses the shortcutName to complete the URL for the gitHub repo to check the current version number against. 

### Output
If a new version is available:
- user is prompted to choose between obtaining the new version or ignoring and continuing

If a new verison is NOT available:
- nothing

## Device/OS Compatibility
- iPhone: ✅ (iOS 16)
- iPad:  ✅ (iPadOS 16)
- Mac:   ✅ (macOS 13 Ventura)
- Apple Watch ✅ (watchOS 9)

## Usage Notes
- Usage is limited to responding to the choice presented if a new version is available
- No configuration is required

## Release Notes
### Version 1.0
*Created by Damian Cavanagh in August 2023*
- Original functionality

