Rails app to interact with MS Onenote

onenote.smithwebtek.com

set up nginx to direct that subdomain to the onenote config file 

work daily in onenote, have it searchable and visual on secured site
use devise for access
manage delegated access, to shared notebooks


created onenote directory on same server as smithwebtek.com
edit nginx config to point requests of that subdomain, to that app

request for onenote.smithwebtek.com >> /home/deploy/onenote

use Capistrano to deploy it

ms demo repo: https://github.com/microsoftgraph/msgraph-training-rubyrailsapp


def ms_graph_urls
"https://graph.microsoft.com/v1.0/me/onenote/{notebooks | sections | sectionGroups | pages} "
"https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages}"
"https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages}"
https://docs.microsoft.com/en-us/azure/active-directory/develop/microsoft-graph-intro
Microsoft Graph API
02/13/2020
2 minutes to read
The Microsoft Graph API is a RESTful web API that enables you to access Microsoft Cloud service resources. After you register your app and get authentication tokens for a user or service, you can make requests to the Microsoft Graph API. For more information, see Overview of Microsoft Graph.
Microsoft Graph exposes REST APIs and client libraries to access data on the following Microsoft 365 services:
Office 365 services: Delve, Excel, Microsoft Bookings, Microsoft Teams, OneDrive, OneNote, Outlook/Exchange, Planner, and SharePoint
Enterprise Mobility and Security services: Advanced Threat Analytics, Advanced Threat Protection, Azure Active Directory, Identity Manager, and Intune
Windows 10 services: activities, devices, notifications
Dynamics 365 Business Central
