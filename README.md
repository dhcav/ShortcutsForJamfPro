# jamfAppSourcer

This Shortcut is designed to simplify determining the optimal packaging workflow for a list of apps by listing availability of the given title/s in the four auto-packaging/distribution utilities listed below. While this is not a common task for most production environments, it is a regular chore for Jamf *partners* such as consultants, MSPs etc supporting our customers.

If a full match is not found, the Shortcut will attempt to match the first word to indicate the need to investigate further. 

This Shortcut is intended to run by itself and does not relate directly to any other Shortcuts. 

### Input
- List of application titles in CSV format (single column, no header)

### Auto-packaging Sources
- Installomator
- Jamf App Installers
- Jamf Patch Management
- Mac App Store

### Output
- Search Results (Yes/Partial/No in Rich Text)

#### Export Results as:
- CSV (plain text)
- PDF (rich text)
- HTML (rich text)
- PNG (rich text)

## Device/OS Compatibility
- iPhone: ✅ (iOS 16)
- iPad:  ✅ (iPadOS 16)
- Mac:   ✅ (macOS 13 Ventura)
- Apple Watch ❌

## How to Use
#### From Finder/Files (anywhere you can right-click or share the .csv)
1. Right click on .csv file and select Quick Actions (Mac) or tap Share button (mobile)
2. Select this Shortcut
3. View Preview (HTML)
4. Choose format to save/share

#### Standalone (from Shortcuts or Menu Bar)
1. Run the Shortcut
2. Select the .csv file as prompted
3. View Preview (HTML)
4. Choose format to save/share

## Usage Notes
- Requires Jamf Pro version 10.39
- Please use a single column .csv with this Shortcut containing app titles **ONLY**
- Future version will include adding vendor names to commonly used and mis-titled apps (e.g. Photoshop to Adobe Photoshop, Office 365 to Microsoft Office 365) to reduce false negatives 
- Installomator and MAS titles are derived directly from the source on run
- Jamf Patch Management titles are not anywhere I can find them to derive programmatically so I’ll endeavour to update the GitHub .txt file after new titles are announced alongside Jamf Pro updatees (nbd: I’ve made another Shortcut to automate it as far as possible 😎)
- The Results preview renders somewhat smaller on iPhone and I’ll address this in a future version
- As always, please provide feedback if you encounter any issues

## Release Notes
### Version 1.2
*Updated by Damian Cavanagh in January 2024*

Included in this update:
- Now retrieve Jamf App Installers titles list programmatically via API on run! 
  - No more manual maintenance of the list on my GitHub! 🥳
  - Credit to ([@tyler-tee](https://github.com/tyler-tee)) for sharing [these (currently) undocumented Jamf App Installers endpoints at JNUC23](https://github.com/tyler-tee/JNUC-2023")
  - Thanks to ([@daniel-maclaughlin](https://github.com/daniel-maclaughlin)) for putting me on to it and reminding me I didn't make it that far through my JNUC watchlist
- Added support for new [shortcutVersioner](https://github.com/dhcav/ShortcutsForJamfPro/tree/main/shortcutVersioner) workflow
  - If there's a new version, you'll be given a choice to install (with one click/tap!!!) or ignore and continue with your installed version 
- Added support for new [helperShortcutChecker](https://github.com/dhcav/ShortcutsForJamfPro/tree/main/helperShortcutChecker) workflow
  - Currently only used for shortcutVersioner, but likely to be used heavily in future versions
  
### Version 1.1
*Updated by Damian Cavanagh in August 2023*

Included in this update:
- added Jamf Patch Management as package source (feature request by [@marcusransom](https://github.com/marcusransom))
- added new 'key' section to results preview (two Jamf sources but neither have an official logo/icon that folks could recognise)
- updated Jamf App Installers and Patch Management list location to [shortcutsForJamfPro/helperFiles](https://github.com/dhcav/ShortcutsForJamfPro/tree/main/helperFiles) (moved from separate repo)
- replaced comprehensive Shortcut notes in comment with basic notes and link to GitHub folder for full info
- resolved error with text replacement when converting .csv results into rich text (will now only replace the result text and not partially replace app name strings with emoji)
- fixed error in which check for 'Partial Match' on Jamf App Installers was operating on incorrect variable and always resulted in Partial match - meaning no app ever received the 'No Match' result for this source

### Version 1.0
*Created by Damian Cavanagh in July 2023*
