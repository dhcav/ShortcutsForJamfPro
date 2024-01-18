# getJamfProUrlAndToken_server_apiClient

***Created by Damian Cavanagh in January 2024***

This helper Shortcut obtains a Bearer Token to authorize later API calls, and also provides the Jamf Pro URL. 

## Download This Shortcut
- You can download this Shortcut [here](https://github.com/dhcav/ShortcutsForJamfPro/raw/main/getJamfProUrlAndToken_server_apiClient/getJamfProUrlAndToken_server_apiClient.shortcut)
- It can also be downloaded by clicking the Shortcut file above, then clicking 'View Raw'


### Input/s
None 
- But you must populate the Shortcut prior to first run with the API Client ID and secret along with your full Jamf Pro URL.  

### Operation
- The Shortcut obtains the Bearer Token, and combines it into a dictionary with the Jamf Pro URL used.

### Output/s
JSON (dictionary)
- A simple dictionary with key/value pairs for `token` and `jamfProURL`, which can be set as variables in the main Shortcut with the 'Get Dictionary value' Action


### Required Privileges
- None


## Device/OS Compatibility
*OS versions listed below have been tested working. Earlier versions are assumed to be compatible given the basic nature of Actions used (most if not all date back to the Workflow days)*
- iPhone: 		✅ (iOS 17)
- iPad:  		✅ (iPadOS 17)
- Mac:  		✅ (macOS 14 Sonoma)
- Apple Watch: 	✅ (watchOS 10)


## Usage Notes
- Use this helper Shortcut with the 'Run Shortcut' Action
- I strongly recommend creating multiple versions of this Shortcut with different privilege sets
- Other than that it's pretty simple so there's no versioning support required


## Release Notes
### Version 1.0
*Created in January 2024*
- Original functionality
- Simpler, earlier versions of this concept dating back to August 2023 can be found in the previousVersions folder
