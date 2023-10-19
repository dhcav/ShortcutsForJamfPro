# getBearerToken

These Shortcuts demonstrate retrieval of the Bearer Token for API authentication. None of them are acceptably secure by modern standards, although running on a trusted device secured with a passcode may not present huge issues for some uses. 

Until Jamf create an app that can provide authenticated Actions into Shortcuts, workflows like this will have to suffice...

## getBearerToken_apiClient_shareable
This Shortcut is currently the most secure way of authenticating for API calls, using the new (10.50) API Role/Client method. 

It could only be improved by using an app like Data Jar to store the Client Secret/Password (as used in the next Shortcut...) 

## getBearerToken_account_shareable_dj
This Shortcut uses Basic Auth to obtain the Bearer Token, with credentials stored in Data Jar (an excellent, free app by Simon Støvring that you can get [here](https://apps.apple.com/au/app/data-jar/id1453273600)).

Within Data jar, I have created a system for storing the credentials of multiple Jamf servers, with support for multiple API accounts for different purposes in each. It's essentially an ecosystem of stored credentials, supported by 'helper' Shortcuts to check which server is "active". 

As much as I love what I've come up with, I will be over the moon when Jamf sherlocks/recreates it. 

## getBearerToken_account_shareable_pt
This Shortcut is the simplest type of Bearer Token retrieval, and also the least secure. For educational purpsoes only. 

Most of my Shortcuts released up til this point (October 2023) have regrettably used this method to simplify usage and testing by admins unfamiliar with Shortcuts' advanced features. 

