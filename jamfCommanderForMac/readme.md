# jamfCommanderForMac

These Shortcuts send commands to Macs, with a variety of input methods supported. 

They are intended to run by themselves and do not relate directly to any other Shortcuts. 

## Download This Shortcut
- You can download this Shortcut [here](https://github.com/dhcav/ShortcutsForJamfPro/raw/main/jamfCommanderForMac/jamfCommanderForMac.shortcut)
- It can also be downloaded by clicking the Shortcut file above, then clicking 'View Raw'


### Inputs
- Choose Group - all smart and static computer_groups, or
- Enter (or paste) serialNumber/s (up to 100), or
- Scan serialNumber QR code/s (up to 100), or
- Scan assetTag QR code/s (up to 100), or
- Individual Mac from Jamf Pro GUI browser page (scrapes id from URL)

*Note: input type is specified in the Shortcut name after the underscore*

### Commands Supported:
- UnmanageDevice
- BlankPush
- SettingsEnableBluetooth
- SettingsDisableBluetooth
- EnableRemoteDesktop
- DisableRemoteDesktop
- DeviceLock (Shortcut will request 6-digit code)
- EraseDevice (Shortcut will request 6-digit code)

### Output
- Chosen command applied to chosen Mac/s

## Device/OS Compatibility
#### jamfCommanderForMac_chooseGroup
- iPhone: ✅ (iOS 16)
- iPad:  ✅ (iPadOS 16)
- Mac:   ✅ (macOS 13 Ventura)
- Apple Watch ⁉️ (given this is simply API calls and choosing from lists, it should work on Apple Watch but initial testing seems to result in an SSL error. Will fix if possible but more of a flex than required functionality so not high priority.)

#### jamfCommanderForMac_enterSerialNumber
- iPhone: ✅ (iOS 16)
- iPad:  ✅ (iPadOS 16)
- Mac:   ✅ (macOS 13 Ventura)
- Apple Watch ✅ (watchOS 9 - Note: tested on a Series 5 only and worked but *very* slow)

#### jamfCommanderForMac_serialNumberQR
- iPhone: ✅ (iOS 16)
- iPad:  ✅ (iPadOS 16)
- Mac:   ❌
- Apple Watch ❌

#### jamfCommanderForMac_assetTagQR
- iPhone: ✅ (iOS 16)
- iPad:  ✅ (iPadOS 16)
- Mac:   ❌
- Apple Watch ❌

#### jamfCommanderForMac_webPage
- iPhone: ✅ (iOS 16)
- iPad:  ✅ (iPadOS 16)
- Mac:   ✅ (macOS 13 Ventura)
- Apple Watch ❌


## How to Use
#### jamfCommanderForMac_chooseGroup
1. Run the Shortcut
2. Choose Group
3. Choose command

#### jamfCommanderForMac_enterSerialNumber
1. Run Shortcut
2. Enter (or paste) serialNumber/s
3. Choose command

#### jamfCommanderForMac_serialNumberQR
1. Run Shortcut to be prompted for QR scan
2. Choose to add more scans if desired
3. Choose command

#### jamfCommanderForMac_assetTagQR
1. Run Shortcut to be prompted for QR scan
2. Choose to add more scans if desired
3. Choose command

#### jamfCommanderForMac_webPage
1. When viewing computer record in browser, click the Menu Bar icon (Mac) or share button (mobile)
2. Select this Shortcut
3. Choose command

*Note: if already in the GUI, it's obviously very easy to click into the management tab and send a command manually - this is more a Proof of Concept than something I think folks will get a lot of usage out of.*


## Usage Notes
- QR versions will also work with barcodes, however (despite it being literally the same action) Shortcuts' barcode scanning ability is *far less reliable* 
- Use the testDeviceQR Shortcut to test QR versions without needing to print
- Any of these Shortcuts could be adapted to apply a single command without requiring the choice
- I ***strongly*** advise you to explore the feasability of adding QR codes to your physical asset tags
  - far superior ease of scanning compared to bar codes as noted above
  - long-distance scanning (I have successfully scanned QRs from up to 3m/10ft away)
- 6-digit codes for deviceLock and eraseDevice commands are not strictly required for Macs with Apple Silicon, however this step has been included simply as a way to allow a final sanity check before applying these powerful commands

## Release Notes
### Version 1.0
*Created by Damian Cavanagh in August 2023*

