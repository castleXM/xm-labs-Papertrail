
# xMatters Comm Plan for Papertrail
This xMatters Comm Plan receives and processes notifications from Papertrail. It's a one way integration at this time.

# Pre-Requisites
* A Papertrail account (https://papertrailapp.com).
* xMatters account - If you don't have one, [get one](https://www.xmatters.com)!

# Files
* [Papertrailv1.zip](Papertrailv1.zip) - The comm plan (if needed) 

# How it works

This integration uses a generic Papertrail Webhook integration. When a Papertrail alert fires for a saved search, it will trigger a call into the xMatters Inbound Integration specified by this Comm Plan. The integration script then parses out the payload and builds an event and passes that to xMatters. 

# Installation
1. Configure a Saved Search in Papertrail

Here's a screencap from the AppMon client Server Settings page that shows you how to install plugins:

<kbd>
  <img src="media/appMonInstallPlugin.PNG" alt="Installing the AppMon Plugin" height="400">
</kbd>

2. Ensure that this Comm Plan has been deployed into xMatters. For help on configuring Comm Plans, please see this link:
https://help.xmatters.com/OnDemand/xmodwelcome/communicationplanbuilder/exportcommplan.htm

Ensure that you've
   
# Testing
How to test

<kbd>
  <img src="media/appMonTestPlugin.PNG" alt="Testing the AppMon Plugin" height="400">
</kbd>

You should be able to see an event in the xMatters Reports page.

