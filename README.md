
# xMatters Comm Plan for Papertrail
This xMatters Comm Plan provides a one way integration with Papertrail. It processes Papertrail events and provides xMatters notifications and response options.

---------

<kbd>
  <a href="https://support.xmatters.com/hc/en-us/community/topics">
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
  </a>
</kbd>

---------

An updated version of this integration is available, supporting the latest version of SolarWinds Papertrail and based on xMatters Flow Designer so you can easily connect other tools to your toolchain. Install it right from the Workflow Template directory within your xMatters instance. [Learn more](http://help.xmatters.com/integrations/#cshid=Papertrail).

---------

# Pre-Requisites
* A Papertrail account (https://papertrailapp.com).
* xMatters account - If you don't have one, [get one](https://www.xmatters.com)!

# Files
* [Papertrailv1.zip](Papertrailv1.zip) - The xMatters Workflow

# How it works

This integration uses a generic Papertrail Webhook integration. When a Papertrail alert fires for a saved search, it will trigger a call into the xMatters Inbound Integration specified by this Workflow. The integration script then parses out the payload and builds an event and passes that to xMatters. 

# Installation
1. Configure a Saved Search in Papertrail, then an alert based off the search. Here's a screencap from Papertrail's Edit Alert screen:

<kbd>
  <img src="media/papertrail.PNG" alt="Configuring an Alert in Papertrail" height="400">
</kbd>

2. Ensure that the Papertrail v1 Workflow has been deployed into xMatters. For help on configuring Workflows, please see this link:
https://help.xmatters.com/OnDemand/xmodwelcome/communicationplanbuilder/exportcommplan.htm

3. Ensure that you've set proper recipient information in the Workflow's PapertrailInboundWebhook form.

4. Copy the URL from the InboundPapertrailWebhook inbound integration in the Workflow.

5. Paste this URL into the Papertrail Edit Alert screen in the Webhook Details area (see screencap).
   
# Testing
Use the 'Send Test Data' button at the bottom of the Papertrail Edit Alert screen. You should be able to see an event in the xMatters Reports page.

