# ShortcutsForJamfPro
A collection of Shortcuts for iOS, iPadOS, macOS and even sometimes watchOS to be used with Jamf Pro. 

Each Shortcut is available in its own folder above, with its own readme to cover specific information. Read on below for general notes...

## Shortcut Compatibility
### Operating Systems
Most if not all Actions used in my Shortcuts date back to the Workflow days, so OS compatibility is not expected to be an issue. 

Each Shortcut will list the OSs they've been test on, but this is not something you should spend a lot of time worrying about. 

### Devices
Where possible, these Shortcuts will be device-agnostic in only using Actions that are present on all supported OSs (e.g. avoiding Mac-only Actions). 

However, certain key Actions for workflows, such as QR Code scanning or NFC reading, may be used and will be noted if so.

## Shortcut Operation
### Shortcuts as Functions/Helper Shortcuts
From the moment I created this repo, I have agonised over this issue. I have for years been using the `Run Shortcut` Action to modularise certain functionality, and it is objectively and unassailably the smart way to be a Shortcuts power user. 

But the spectre of Shortcut failure issues for new users that didn't understand which 'helper Shortcuts' they needed took me down the path of recreating every Shortcut Action by Action. Which honestly has been excruciating and definitely made getting a release together far more difficult. 

Given this background, I am beyond excited to share that I have cracked this particular nut with [helperShortcutChecker](https://github.com/dhcav/ShortcutsForJamfPro/tree/main/helperShortcutChecker)!!!

See its readme for more details, but essentially it will check that all helper Shortcuts required for a main Shortcut are present in your library and if not, the main Shortcut will auto-download and open them so the user simply has to tap/click 'Add Shortcut' before it continues without issue.

This particular issue has had a significant impact on my releases, so it's difficult to overstate how satisfying it is to have come up with an effective workflow. 

### Third-party Apps
To facilitate the wider uptake of Shortcuts amongst the Mac Admin community, and reduce potential complications, I have largely avoided any usage of Actions from third-party apps. 

If I can't avoid it, I will endeavour to use free apps. Most of my favourite Shortcuts Utility apps (e.g. Data Jar, Toolbox Pro, Secure Shellfish, Actions, Charty, Pushcut) are either entirely free or include good functionality without requiring an in-app purchase. 

## Versioning
Another key issue I've encountered since starting this repo that seems to be taken care of thanks to the new support for helper Shortcuts!

[shortcutVersioner](https://github.com/dhcav/ShortcutsForJamfPro/tree/main/shortcutVersioner) checks the installed version against the latest version, stored in the version.json dictionary in each Shortcut's folder. If a newer version is available, the user will be prompted to download and install it, or can ignore and continue with their current version. 

There's a bit more to it than that so see the link above, but again, having a solid solution to a long-term problem that was only going to compound further as time went by is a great feeling.

Even with my significant head start compared to most (all?) Mac Admins, I'm learning more about Shortcuts every day and I'd hate to think members of our time-poor, hard-working community might not be saving as much time as possible just because they didn't know a new and improved version had been released. 

## Security
### Authentication
I used quite strong language in this section of the original version of this readme. 

It is still true that until there is a Jamf Shortcuts app to provide auth via approved Actions, we can't avoid having credentials appear in plain text.

But in the meantime, Jamf's new API Role/Client authentication option has effectively eliminated the risk of credentials improperly shared within a Shortcut being used to access the Jamf Pro GUI. And now that helper Shortcuts are in play, setting one up with your Client ID and Secret to generate the token and pass through to the main Shortcut is a piece of cake. 

Of course I wouldn't make you create one from scratch though. See [getJamfProUrlAndToken_server_apiClient](https://github.com/dhcav/ShortcutsForJamfPro/tree/main/getJamfProUrlAndToken_server_apiClient) for more info. 

I highly recommend creating multiple versions of this Shortcut to cover varying privilege sets, which would simply be renamed with the first element of your Jamf Pro URL, then the API client being used.

An 'import question' to prompt for the name of the desired version of getJamfProUrlAndToken is included in all new Shortcuts and being added to older Shortcuts as time permits.

Finally, the added bonus of this approach is that it's a convenient place to record your Jamf Server URL - meaning any main Shortcut is entirely free of identifying information!!! 

### Privileges
Another new Shortcut to make this chore easier! apiRoleCreator will retrieve the full list of privileges, allow you to select any or all of them, then create a new API Role. It'll even take you  straight to the 'new API Client' page in the GUI to quickly add the role and grab the credentials, or the API Client tab to add it to an existing client. 

What's more, I'll now be updating each Shortcut's readme to clearly list required privileges, and if I'm feeling really energised I'll actually just make a version of apiRoleCreator for each one that you can quickly run and add to your client of choice.


## Tips, Troubleshooting & Known Issues:
- Use folders for each Shortcut if editing/altering them. Trust me.
- When creating, testing, or refining Shortcuts, consider creating a new version before making major changes. 
- There is an almost endless undo ability within Shortcuts *until* you close and reopen it. Be mindful of this if working on complex Shortcuts
- The Mac app seems to encounter issues far more than the mobile version. Consider restarting the app at the first sign of lag dragging Actions around, beachballing on runs, or any other quirks


### Feedback
I said "we're essentially in the pre-history of Shortcuts being used for Mac Admin workflows" in the original version of this readme. 

WWDC23 changed that. Bigtime. 

But it's still early days, and as mentioned above, my own abilities with Shortcuts are ever-evolving. And the momentum building in the wider community seems to be growing too.

As such, please send tips, feature/Shortcuts requests or other feedback on any issues that you encounter with these Shortcuts as issues here on GitHub, or via the Mac Admins Slack (I'm @d.cav).

There are plenty of Mac Admins with more experience and technical knowledge than me, and I can't wait to see what they (you?) come up with. 
