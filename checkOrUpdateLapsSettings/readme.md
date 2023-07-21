# checkOrUpdateLapsSettings

*Created by Damian Cavanagh in June 2023.*

This Shortcut retrieves the current LAPS configuration and displays to user, and provides the ability to modify any or all or the values or retain current settings.

This functionality was introduced in Jamf Pro 10.46 but is not yet supported in the GUI, so using this Shortcut is a simple way to enable this excellent feature without knowing how to make curl commands in Terminal (or using other API tools). 

After running this Shortcut, use my [getLapsPassword-Webpage](https://github.com/dhcav/ShortcutsForJamfPro/blob/main/getLapsPassword-Webpage/getLapsPassword-WebPage.jpa.mac.mm.shortcut) Shortcut to retrieve the password for a given Mac.

## Device Compatibility
- iPhone: Yes
- iPad: Yes
- Mac: Yes
- Apple Watch: Yes

## Notes
- requires Jamf Pro version 10.46
- if the Import Questions don’t work, the Shortcut will fail - be sure to check the correct fields below have been populated if you encounter an error on first run
