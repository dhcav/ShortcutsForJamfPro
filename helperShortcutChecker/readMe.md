# helperShortcutChecker

***Created by Damian Cavanagh in January 2024***

This helper Shortcut checks if Shortcuts used in a main Shortcut's `Run Shortcut` Action (like a function) are installed, automatically downloads them from GitHub if not found, and opens them in Shortcuts to present the user with a one-tap/one-click option to install. 

NOTE: Having finally devised an effective solution for using Shortcuts like functions, as I have been for years in my personal usage, I no longer have to deal with the excruciating task of recreating helper Shortcuts Action by Action. This is by far the superior approach, as even the biggest and most complex Shortcuts are largely reduced to inputs and outputs of the `Run Shortcut` Action. THIS IS A BIG DEAL FOR ME.

## Download This Shortcut
- You can download this Shortcut [here](https://github.com/dhcav/ShortcutsForJamfPro/raw/main/helperShortcutChecker/helperShortcutChecker.shortcut)
- It can also be downloaded by clicking the Shortcut file above, then clicking 'View Raw'


### Input/s
`string` (A Shortcut's name)

*helperShortcutChecker is designed to be used with a Shortcut name provided as input to the `Run Shortcut` Action. If run without input, it will prompt the user to retrieve the clipboard or enter text* 

### Operation
- Each main Shortcut using `helperShortcutChecker` will contain a small dictionary, with a key/value pair for each helper Shortcut in the format: `"shortcutName": "downloadURL"`
- All keys (Shortcut names) will be iterated through `helperShortcutChecker`, returning `true` if the Shortcut is found and `false` if not

### Output/s
Boolean: `true`/`false`
- If a `false` response is received, logic in the main Shortcut will download the missing Shortcut from its downloadURL and open the file, presenting the user with the `Add Shortcut` popup
- The main Shortcut will wait for 5 seconds for the user to tap/click 'Add Shortcut' before continuing


### Required Privileges
- None (no Jamf API usage)


## Device/OS Compatibility
*OS versions listed below have been tested working. Earlier versions are assumed to be compatible given the basic nature of Actions used (most if not all date back to the Workflow days)*
- iPhone: 		✅ (iOS 17)
- iPad:  		✅ (iPadOS 17)
- Mac:  		✅ (macOS 14 Sonoma)
- Apple Watch: 	✅ (watchOS 10)


## Usage Notes
- Shortcuts using this workflow actually need to check if helperShortcutChecker is present, which for obvious reasons is achieved Action by Action before this Shortcut can be used with `Run Shortcut` 
- No configuration is required
- This Shortcut will not use shortcutVersioner given its simplicity. If better ways of handling the task come to me, I'll avoid breaking changes and ensure the `true`/`false` output is maintained
- For a time, I considered having a variable saved locally on the device to indicate `true` if all Shortcuts were found, which could be used for logic that would skip the check if so. However on reflection I realised that the *minor* 2-4 second delay it caused in my testing was due to having nearly 1,300 Shortcuts in my library, and there's probably only a dozen people on the planet that might experience similar performance issues. (But I'll probably still do it eventually just because it's super sweet.)


## Release Notes
### Version 1.0
*Created in January 2024*
- Original functionality as per notes above
