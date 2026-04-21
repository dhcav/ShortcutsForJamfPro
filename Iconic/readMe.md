Iconic

For Jamf Pro

Created by Damian Cavanagh in May 2024

This Shortcut is designed for use with my iconicForJamfPro workflow by retrieving the iconicForJamfPro ‘script’, which is a JSON dictionary that stores icon attributes (name, Jamf Pro ID, URL, and base64-encoded thumbnail image) for easier re-use. 

The main benefit of this approach is that it enables programmatic retrieval of the icon’s URL/Jamf Pro ID for re-use after initial upload, e.g. for Jamf Setup Manager, 

Existing icon attributes are used to populate a visual menu from which to choose the desired icon, then select an attribute to copy to clipboard. 

Third party app requirements:
- For Mac, you need Jamf Actions, signed in with an account or API Client
- For mobile devices, you need PocketMDM, signed in with an account or API Client

Jamf Pro privilege requirements:
- Read Scripts
- Update Scripts
- Create Scripts
- Read Categories
- Create Categories
- Read Icons
- Create Icons
