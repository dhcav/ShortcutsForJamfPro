# apiRoleCreator

***Created by Damian Cavanagh in January 2024***

This Shortcut creates API Roles in Jamf Pro. It will allow the user to select privileges from the full list (retrieved on run) and create the role with a POST command. 


### Input/s
- None

### Operation
- User is prompted to enter a displayName for the API Role
- The full privilege list is retrieved
- User is presented with the privilege list to select from (multiple selections suported)
- Variables are combined into a JSON payload and POST command is made to create the API Role

### Output/s
- New API Role in Jamf Pro

After Role creation is complete, the user is prompted to choose between:
- creating a new API Client to add the new API Role to (Jamf Pro GUI)
- opening the API Client tab to select and existing API Client to add the new API Role to (Jamf Pro GUI)
- taking no immediate action (to add the API Role to a client later)


### Required Privileges
- Read API Roles
- Create API Roles


## Device/OS Compatibility
*OS versions listed below have been tested working. Earlier versions are assumed to be compatible given the basic nature of Actions used (most if not all date back to the Workflow days)*
- iPhone: 		✅ (iOS 17)
- iPad:  		✅ (iPadOS 17)
- Mac:  		✅ (macOS 14 Sonoma)
- Apple Watch: 	❌


## Usage Notes
- It does what it says on the tin, not much to add
- Choosing the 'new API Client' or 'view API Clients' options after API Role Creation takes you directly to your Jamf Pro instance in default browser - if not already logged in you'll just be taken to the dashboard


## Release Notes
### Version 1.0
*Created in January 2024*
- Original functionality as above
