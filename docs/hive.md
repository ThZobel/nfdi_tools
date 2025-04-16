# The HIVE - FAQ
=================

## Introduction
---------------

Every work group can apply for an account on the HIVE. Please ask your PI or a responsible person in your lab if you already have an account. If you do not have an account yet, please ask your PI or the official contact person of the Imaging Network to contact the Imaging Network. We will then create an account for you.

## Connecting to the HIVE
-------------------------

To connect to the HIVE, you can use the remote desktop connection. This is also possible from home via the university VPN connection.

1. Start the Remote Desktop Control and connect to the following IP address: `10.15.127.4`
2. Enter the following information into the empty fields:
	* Username: `<Account_Name>`
	* Password: `<Account-Password>`
3. It may be necessary to activate the "Use a different account" option.

## Mounting Network Drives
---------------------------

We recommend using a network share of the WWU-Cloud, as the HIVE has a high-speed connection to it.

### On the HIVE

1. Open the Windows Explorer on the HIVE and go to "This PC".
2. Use the "Map Network Drive" function and enter the following path: `\\\\wwu.de\ddfs\Cloud\wwu1\<Project_Name>\<Share-Name>`
3. Check the "Connect using different credentials" option.

### On a Normal PC in the WWU Network

1. Open the Windows Explorer and go to "This PC".
2. Use the "Map Network Drive" function and enter the following path: `\\\\wwu.de\ddfs\Cloud\wwu1\e_min\Data`
3. Check the "Connect using different credentials" option.
4. Press Finish. In the next window, use your university ID and central university password to connect to your network share.
	* Username: `wwu\<University-ID>`
	* Password: `<University-Password>`

## Project Folders
--------------------

Each account on the HIVE has a project folder on the RAID5 system: `D:\PROJECTS\<workgroup name>`

You can mount this folder as a network drive using: `\\10.15.127.4\<workgroup name>`

## Accessing Your Data
----------------------

If you don't have access to your network drive, there are two main options:

1. Use Sciebo
2. Temporarily save your data on the network share of the Imaging Network.

To connect to the network share of the Imaging Network, use the "Map Network Drive" function and connect to the following path:

* From Windows: `\\\\wwu.de\ddfs\Cloud\wwu1\e_min\data`
* From Linux/Mac: `\\\\zivdfs1.wwu.de\ddfs\Cloud\wwu1\e_min\data`
* From the HIVE: `\\\\zivdfs1.wwu.de\openstack\e_min\data`

Login data:
* Username: `wwu\<University-ID>`
* Password: `<University-Password>`

## Troubleshooting
------------------

If you have any issues or questions, please use the Mattermost channel of the Imaging Network or send us a private message via Mattermost or email. Contact information is available on the homepage of the Imaging Network.

## Display Settings
-------------------

To use multiple monitors, simply enlarge the option when connecting to the HIVE:

1. Under Display, activate the "Use all my monitors..." function.
