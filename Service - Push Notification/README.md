![IRD logo](../Images/IRlogo.gif)
![Software Dev](../Images/SoftwareDev.png)

# Return Status Push Notifications Service 

The Return Status Push Notification file is intended to be used by software providers where large quantities of return status data is required. 

The Return Status Push Notification is based around a file transfer solution, where Inland Revenue will send information via SFTP to the software provider on a daily (overnight) basis in the evening of each business day.  

## Key documentation

- Build pack
	- Download and view the [Push Notifications build pack](Gateway%20Services%20Build%20Pack%20-%20Push%20Notifications.pdf)

- Schemas
	- View and download the [common v2 xsd](../Common%20XSD/Common.v2.xsd)
	- View and download the [return service common v2 xsd](../Common%20XSD/ReturnCommon.v2.xsd)
	- View and download the [Return Status Push Notifications v1 xsd](ReturnStatusPushNotifications.v1.xsd) from this current directory	
	
## Return Status Push Notification ZIP/XML sample files

* [ZIP file:](Sample%20Files/PSN_DAILY_PROVIDER_1500216000_2155445580_2155445927_201909091028315313_NZX.zip) `PSN_DAILY_PROVIDER_1500216000_2155445580_2155445927_201909091028315313_NZX.zip`
    * DAILY AGENT File `PSN_DAILY_AGENT_IRD_132349932_2155445580_2155445927_201909091028315782_NZX.xml`
	* DAILY CUSTOMER File `PSN_DAILY_CUSTOMER_2155445580_2155445927_201909091028315782_NZX.xml`
* [XML Control File](Sample%20Files/PSN_DAILY_PROVIDER_1500216000_2155445580_2155445927_201909091028316719_NZX_CONTROL.xml)  `PSN_DAILY_PROVIDER_1500216000_2155445580_2155445927_201909091028316719_NZX_CONTROL.xml`

> NOTE: The real production and non-production the XML and ZIP files will be PGP encrypted.

## Access information 

* Software Providers needs to provide the following:
	* IP Address and port number for a SFTP server
	* SFTP Username and Password 
	* SFTP remote directory 
	* Public PGP key - used for payload encryption (See [openpgp.org](openpgp.org) for more information)
	
* The On-boarding Team will provide a 
	* SSH Keys for SFTP Public Key Authentication 

## Supporting services

* [Service: Income Tax](../Service%20-%20Income%20Tax/) - for filing of Income Tax returns
* [Service: Identity and Access](https://github.com/InlandRevenue/Gateway_Services-Access/tree/master/Identity%20and%20Access) – for additional details on SSH and PGP authentication information.
* [Service: Intermediation](https://github.com/InlandRevenue/Gateway_Services-Access/tree/master/Service%20-%20Intermediation) – for managing links between business intermediaries and their client lists and their customer accounts.
* [Service: Software Intermediation](https://github.com/InlandRevenue/Gateway_Services-Access/tree/master/Service%20-%20Software%20Intermediation) – for service providers to manage links to tax intermediary clients or directly to customers through their software


