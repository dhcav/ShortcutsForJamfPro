# shortcutVersioner

***Created by Damian Cavanagh in August 2023***

This helper Shortcut checks the currentVersion of the main Shortcut (from which it is run like a function using the Run Shortcut action) against the version.json dictionary in the main Shortcut's folder on GitHub. 


### Input/s
Each main Shortcut will provide a small dictionary to shortcutVersioner, containing:
- shortcutName
- currentVersion
*shortcutVersioner requires this dictionary as input and will not run without it* 

### Operation
- Use the provided shortcutName to complete the URL to access version.json in the main Shortcut's GitHub folder (an example dictionary is included in this folder)
- Check currentVersion against latestVersion
  - If a newer version is available, the number and release notes will be presented to the user along with a choice to download and install the new version then exit the main Shortcut, or ignore and proceed with current version
  - If no newer version is available, or if the ignore option is selected, nothing will happen and the main Shortcut will continue

### Output/s
Boolean: true/false
- All main Shortcuts using this workflow include logic to determine if a new version has been downloaded, and will exit if so. 


### Required Privileges
- None (no Jamf API usage)


## Device/OS Compatibility
*OS versions listed below have been tested working. Earlier versions are assumed to be compatible given the basic nature of Actions used (most if not all date back to the Workflow days)*
- iPhone: 		✅ (iOS 17)
- iPad:  		✅ (iPadOS 17)
- Mac:  		✅ (macOS 14 Sonoma)
- Apple Watch: 	✅ (watchOS 10)


## Usage Notes
- Usage is limited to responding to the choice presented if a new version is available
- No configuration is required


## Release Notes
### Version 1.1
*Released in January 2024*
- various user communication enhancements
- added logic to handle exiting the main Shortcut

### Version 1.0
*Created in August 2023*
- Original functionality
