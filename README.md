# ObjectCreation
GUI to create new object with templates or in batches

## Description

One task that every systems administrator has to go through at some point is the creation of new object accounts.  Over time, this becomes burdensome and tedious.  The Active Directory wizard takes you through multiple screens and you have to enter the same information multiple times in some occasions (e.g. a lot of organizations use FirstName.LastName for samAccountNames).  It also does not allow you to set all of the fields that you want included in the wizard.  I wanted a way to include those fields and an option to set defaults for some fields.  Luckily Powershell makes all of that possible in an easy to use way.  Powershell does all of the heavy lifting and an optional XML file saves even more time by pre-populating certain fields and setting defaults.  You also have the ability of bulk-adding objects via CSV.  To create objects from a CSV, click on File > CSV Mode.  You can then import the CSV and browse through the objects in the CSV.  Once the CSV is imported, you can create one object at a time or all at once.  If you want a CSV template created for you, click on File > Create CSV Template.

## Features

* Allows object creation with oft-used Active Directory attributes
* Bulk creation of objects from CSV
* Auto-generation of account attributes based on other attributes
  * Display Name
  * samAccountName
  * userPrincipalName
* Default entries
  * Domain
  * OU
  * Phone Number (can use full number or company prefix '212-555-')
  * Department
  * Company
  * Description
  * Password (Accounts are set to change at first logon)
  * Site (HQ, Branch Office 1, etc)
  * Street Address
  * City
  * State
  * Postal Code
  * Address information
  * Domains
  * OUs
  * Descriptions
  * Departments

## Changelog

2.0 - 19.11.2023
* Added Password Never Expire option
* Added Password Cannot Change option
* Change get Current Domain value from csv
* Change get OU value from csv
* Change get Description value from csv
* Change get Departman value from csv
* Change get Site value from csv
* Minor improve code

1.2 - 2012/12/04
* Added check for XML Options file - Will now prompt to create one if not found
* Added XML Options file version check
* Fixed bug where Display Name, sAMAccountName, and UPN were not being generated correctly for CSV files
* Title and Description should be set correctly when creating users from CSV

1.1 - 2012/05/13
* Added ability to select custom format for sAMAccountName, UPN, and Display Name
* Minor bug fixes

1.0 - 2012/03/03
* Updated to be compatible with PowerShell v3
* Enter custom sAMAccountName, Display Name, and userPrincipalName in single-user and CSV modes
* Turn off auto-generation of sAMAccountName, Display Name, and userPrincipalName in single-user mode
* Better error-handling during user creation
* Set new accounts as enabled or disabled
* Set 'Password must change at logon' to enabled or disabled 
* Minor bug fixes
