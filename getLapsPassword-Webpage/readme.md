# getLapsPassword-Webpage

Created by Damian Cavanagh in June 2023

This Shortcut will extract a Mac’s ID from the Jamf Pro URL (when vieweing in browser) and return the LAPS account and password.

## Notes for usage:

### Installation:
- Shortcut is configured to request Jamf Pro account details on install, which can be edited for different servers or accounts in the Text actions below.

### How to use: Mac
1. View the Mac record in browser
2. Tap the Shortcuts icon in the Menu Bar
3. Double-click this Shortcut in the dropdown list to run it

### How to use: Mobile
1. View the Mac record in browser
2. Tap the Share buton 
3. Scroll down to the second block of options to find the Shortcut 
4. Tap to run

### General Notes:
- Mobile testing: working from the Share Menu with Safari and Chrome, other browsers likely to work fine also
- Mac testing: working from the Menu Bar for Safari and Chrome
- Mac with external display/s: the alert window may not pop up on the screen you’ve run the Shortcut from
- Mac Share button: it is possible to click the Share button and run the Shortcut from the list that appears, however this introduces an error that causes extracting the serialNumber to fail, which causes the whole Shortcut to fail. Solution: Use method described above, it’s faster anyway. 
