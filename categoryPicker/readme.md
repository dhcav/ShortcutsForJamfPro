# categoryPicker

***Created by Damian Cavanagh in December 2023***

This helper Shortcut is designed to be used within other Shortcuts where a Category needs to be chosen or created.  

## Download This Shortcut
- You can download this Shortcut [here](https://github.com/dhcav/ShortcutsForJamfPro/raw/main/categoryPicker/categoryPicker.shortcut)
- It can also be downloaded by clicking the Shortcut file above, then clicking 'View Raw'


### Input/s
Optional
- "id" or "name"
  - When running within another Shortcut, users can specify the output type by preceding the 'Run Shortcut' Action with a text Action containing either term then adding that variable as the 'Run Shortcut' input
  - If no Shortcut input is provided, the user is prompted to choose the output type as the final step of the process

### Operation
- The list of current Jamf Pro Categories is retrieved on run
- Category list is displayed to the user to choose from, as well as an option to create a new Category
  - If new, user is prompted for the Category name and priority, and a POST command creates it
- The selected/new Category name is used to retrieve its ID in order to present it to the user in the next step as an output option
- The user is prompted to output the name or ID of the selected/newly created Category

### Output/s
User's choice of:
String: categoryName, or
Integer: categoryID


### Required Privileges
- Read Categories
- Create Categories


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
### Version 1.0
*Created in December 2023*
- Original functionality

