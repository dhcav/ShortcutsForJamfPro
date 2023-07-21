# getLapsPassword-Webpage

Created by Damian Cavanagh in June 2023

This Shortcut will return a Mac's LAPS account and password by extracting its ID from the Jamf Pro URL (when viewing in browser). 

This functionality was introduced in Jamf Pro 10.46 but is not yet supported in the GUI, so LAPS password is currently ***only*** accessible via API. In order for this Shortcut to function you must already have configured your LAPS settings via the API, which you can do with my [checkOrUpdateLAPSSettings](https://github.com/dhcav/ShortcutsForJamfPro/blob/main/checkOrUpdateLapsSettings/checkOrUpdateLapsSettings.jpa.mac.mm.shortcut) Shortcut. 

### How to use: Mac
1. View the Mac record in browser (Any Jamf Pro page that contains the Mac's ID should work)
2. Tap the Shortcuts icon in the Menu Bar
3. Double-click this Shortcut in the dropdown list to run it

### How to use: Mobile
1. View the Mac record in browser (Any Jamf Pro page that contains the Mac's ID should work)
2. Tap the Share buton 
3. Scroll down to the second block of options to find the Shortcut 
4. Tap to run

## Device/OS Compatibility: 
- iPhone: ✅ (iOS 16)
- iPad:  ✅ (iPadOS 16)
- Mac:   ✅ (macOS 13 Ventura)
- Apple Watch:  ❌ 

## Notes:
- requires Jamf Pro version 10.46
- if the Import Questions don’t work, the Shortcut will fail - be sure to check the correct fields below have been poopulated if you encounter an error on first run
- Mobile testing: working from the Share Menu with Safari and Chrome, other browsers likely to work fine also
- Mac testing: working from the Menu Bar for Safari and Chrome
- Mac with external display/s: the alert window may not pop up on the screen you’ve run the Shortcut from
- Mac Share button: it is possible to click the Share button and run the Shortcut from the list that appears, however this seems to introduce an error that causes extracting the serialNumber to fail, which causes the whole Shortcut to fail. Solution: Use method described above, it’s faster anyway... 
