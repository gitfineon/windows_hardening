Windows 10 Hardening
====================

Bit Locker
==========
- [ ] Enable Bit Locker

Antivirus
=========
- [ ] Enable Windows Defender

Group Policies
==============

[CIS Microsoft Windows 10 Enterprise RTM (Release 1507) Benchmark](https://benchmarks.cisecurity.org/tools2/windows/CIS_Microsoft_Windows_10_Enterprise_RTM_Release_1507_Benchmark_v1.0.0.pdf)

Account Policies
----------------
- [ ] Set `Account lockout duration` to `15 or more minute(s)`

  Computer Configuration\Policies\Windows Settings\Security Settings\Account Policies\Account Lockout Policy\Account lockout duration

- [ ] Set `Account lockout threshold` to `10 or fewer invalid logon attempt(s), but not 0

  Computer Configuration\Policies\Windows Settings\Security Settings\Account Policies\Account Lockout Policy\Account lockout threshold

- [ ] Set `Reset account lockout counter after` to `15 or more minute(s)

  Computer Configuration\Policies\Windows Settings\Security Settings\Account Policies\Account Lockout Policy\Reset account lockout counter after

Local Policies
--------------
- [ ] Audit Policy
  - [ ] Audit account logon events: Failure
  - [ ] Audit account management: Success, Failure
  - [ ] Audit directory service access : No auditing
  - [ ] Audit logon events: Failure
  - [ ] Audit object access: Failure
  - [ ] Audit policy change: Success, Failure
  - [ ] Audit privilege use: Success, Failure
  - [ ] Audit process tracking: No auditing
  - [ ] Audit system events: Success Failure



$lp = Computer Configuration\Policies\Windows Settings\Security Settings\Local Policies\
__________________________________________________________________________________

- [ ] Set `Access this computer from the network` to `Administrators` 


  $lp\User Rights Assignment\Access this computer from the network

- [ ] Set `Allow log on locally` to `Administrators, Users`

  $lp\User Rights Assignment\Allow log on locally

- [ ] Set `Deny access to this computer from the network` to include `Guests, Local account`

  $lp\User Rights Assignment\Deny access to this computer from the network

- [ ] Set `Deny log on as a batch job` to include `Guests`

  $lp\User Rights Assignment\Deny log on as a batch job

- [ ] Set `Deny log on as a service` to include `Guests`

  $lp\User Rights Assignment\Deny log on as a service

- [ ] Set `Deny log on through Remote Desktop Services` to include `Guests, Local account`

  $lp\User Rights Assignment\Deny log on through Remote Desktop Services

- [ ] Set `Accounts: Block Microsoft accounts` to `Users can`t add or log on with Microsoft accounts`

  $lp\Security Options\Accounts: Block Microsoft accounts

- [ ] Set `Interactive logon: Do not display last user name` to `Enabled`

  $lp\Security Options\Interactive logon: Do not display last user name

- [ ] Set `Interactive logon: Do not require CTRL+ALT+DEL` to `Disabled` 

  $lp\Security Options\Interactive logon: Do not require CTRL+ALT+DEL

- [ ]  Set `Microsoft network client: Digitally sign communications (always)` to `Enabled`

  $lp\Security Options\Microsoft network client: Digitally sign communications (always)

- [ ] Set `Microsoft network client: Digitally sign communications (if server agrees)` to `Enabled` 

  $lp\Security Options\Microsoft network client: Digitally sign communications (if server agrees)

- [ ] Set `Microsoft network server: Digitally sign communications (always)` to `Enabled`

  $lp\Security Options\Microsoft network server: Digitally sign communications (always)

- [ ] Set `Microsoft network server: Digitally sign communications (if client agrees)` to `Enabled`

  $lp\Security Options\Microsoft network server: Digitally sign communications (if client agrees)

- [ ] Set `Network access: Do not allow anonymous enumeration of SAM accounts and shares` to `Enabled`

  $lp\Security Options\Network access: Do not allow anonymous enumeration of SAM accounts and shares

- [ ] Set `Network access: Do not allow storage of passwords and credentials for network authentication` to `Enabled`

  $lp\Security Options\Network access: Do not allow storage of passwords and credentials for network authentication

- [ ] Set `Network security: LAN Manager authentication level` to `Send NTLMv2 response only. Refuse LM & NTLM` 

  $lp\Security Options\Network security: LAN Manager authentication level

- [ ] Set `Network security: Minimum session security for NTLM SSP based (including secure RPC) clients` to `Require NTLMv2 session security, Require 128-bit encryption`

  $lp\Security Options\Network security: Minimum session security for NTLM SSP based (including secure RPC) clients

- [ ] Set `Network security: Minimum session security for NTLM SSP based (including secure RPC) servers` to `Require NTLMv2 session security, Require 128-bit encryption`

  $lp\Security Options\Network security: Minimum session security for NTLM SSP based (including secure RPC) servers

- [ ] Set `Shutdown: Allow system to be shut down without having to log on` to disabled

  $lp\Security Options\Shutdown: Allow system to be shut down without having to log on

- [ ] Set `User Account Control: Admin Approval Mode for the Built-in Administrator account` to `Enabled`

  $lp\Security Options\User Account Control: Admin Approval Mode for the Built-in Administrator account

Windows Firewall With Advanced Security
---------------------------------------
- [ ] Set `Windows Firewall: Domain: Firewall state` to `On (recommended)`

  Computer Configuration\Policies\Windows Settings\Security Settings\Windows Firewall with Advanced Security\Windows Firewall with Advanced Security\Windows Firewall Properties\*\Firewall state

- [ ] Set `Windows Firewall: Domain: Inbound connections` to `Block (default)`

  Computer Configuration\Policies\Windows Settings\Security Settings\Windows Firewall with Advanced Security\Windows Firewall with Advanced Security\Windows Firewall Properties\*\Inbound connections

Control Panel
-------------
- [ ] Set `Prevent enabling lock screen camera` to `Enabled`

  Computer Configuration\Policies\Administrative Templates\Control Panel\Personalization\Prevent enabling lock screen camera

$adt_sys=Computer Configuration\Policies\Administrative Templates\System\
_________________________________________________________________________

- [ ] Set `Turn off the Windows Messenger Customer Experience Improvement Program` to `Enabled`

  $adt_sys\Internet Communication Management\Internet Communication settings\Turn off the Windows Messenger Customer Experience Improvement Program

- [ ] Set `Turn off Windows Customer Experience Improvement Program` to `Enabled`

  $adt_sys\Internet Communication Management\Internet Communication settings\Turn off Windows Customer Experience Improvement Program

- [ ] Set `Turn off Windows Error Reporting` to `Enabled`

  $adt_sys\Internet Communication Management\Internet Communication settings\Turn off Windows Error Reporting

- [ ] Set `Do not display network selection UI` to `Enabled`

  $adt_sys\Logon\Do not display network selection UI

- [ ] Set `Turn off app notifications on the lock screen` to `Enabled`

  $adt_sys\Logon\Turn off app notifications on the lock screen

- [ ] Set `Untrusted Font Blocking` to `Enabled: Block untrusted fonts and log events`

  $adt_sys\Mitigation Options\Untrusted Font Blocking

- [ ] Set `Allow standby states (S1-S3) when sleeping (on battery)` to `Disabled` 

  $adt_sys\Power Management\Sleep Settings\Allow standby states (S1-S3) when sleeping (on battery)

- [ ] Set `Allow standby states (S1-S3) when sleeping (plugged in)` to `Disabled` 

  $adt_sys\Power Management\Sleep Settings\Allow standby states (S1-S3) when sleeping (plugged in)

- [ ] Set `Require a password when a computer wakes (on battery)` to `Enabled`

  $adt_sys\Power Management\Sleep Settings\Require a password when a computer wakes (on battery)

- [ ] Set `Require a password when a computer wakes (plugged in)` to `Enabled`

  $adt_sys\Power Management\Sleep Settings\Require a password when a computer wakes (plugged in)

- [ ] Set `Configure Offer Remote Assistance` to `Disabled` 

  $adt_sys\Remote Assistance\Configure Offer Remote Assistance

- [ ] Set `Configure Solicited Remote Assistance` to `Disabled`

  $adt_sys\Remote Assistance\Configure Solicited Remote Assistance

- [ ] Set `Enable RPC Endpoint Mapper Client Authentication` to `Enabled`

  $adt_sys\Remote Procedure Call\Enable RPC Endpoint Mapper Client Authentication

- [ ] Set `Restrict Unauthenticated RPC clients` to `Enabled: Authenticated`

  $adt_sys\Remote Procedure Call\Restrict Unauthenticated RPC clients

- [ ] Set `Enable/Disable PerfTrack` to `Disabled`

  $adt_sys\Troubleshooting and Diagnostics\Windows Performance PerfTrack\Enable/Disable PerfTrack

- [ ] Set `Enable Windows NTP Client` to `Enabled` 

  $adt_sys\Windows Time Service\Time Providers\Enable Windows NTP Client

- [ ] Set `Enable Windows NTP Server` to `Disabled`

  $adt_sys\Windows Time Service\Time Providers\Enable Windows NTP Server

$adt_comp=Computer Configuration\Policies\Administrative Templates\Windows Components\
______________________________________________________________________________________

- [ ] Set `Allow a Windows app to share application data between users` to `Disabled`

  $adt_comp\App Package Deployment\Allow a Windows app to share application data between users

- [ ] Set `Block launching Windows Store apps with Windows Runtime API access from hosted content.` to `Enabled`

  $adt_comp\App runtime\Block launching Windows Store apps with Windows Runtime API access from hosted content.

- [ ] Set `Disallow Autoplay for non-volume devices` to `Enabled` 

  $adt_comp\AutoPlay Policies\Disallow Autoplay for non-volume devices

- [ ] Set `Set the default behavior for AutoRun` to `Enabled: Do not execute any autorun commands`

  $adt_comp\AutoPlay Policies\Set the default behavior for AutoRun

- [ ]  Set `Turn off Autoplay` to `Enabled: All drives`

  $adt_comp\AutoPlay Policies\Turn off Autoplay

- [ ]  Set `Allow Secure Boot for integrity validation` to `Enabled`

  $adt_comp\BitLocker Drive Encryption\Operating System Drives\Allow Secure Boot for integrity validation

- [ ] Set `Configure use of hardware-based encryption for operating system drives` to `Enabled`

  $adt_comp\BitLocker Drive Encryption\Operating System Drives\Configure use of hardware-based encryption for operating system drives

- [ ] Configure use of hardware-based encryption for operating system drives: Use BitLocker software-based encryption when hardware encryption is not available`

  $adt_comp\BitLocker Drive Encryption\Operating System Drives\Configure use of hardware-based encryption for operating system drives: Use BitLocker software-based encryption when hardware encryption is not available

- [ ] Set `Require additional authentication at startup` to `Enabled`

  $adt_comp\BitLocker Drive Encryption\Operating System Drives\Require additional authentication at startup

- [ ] Set `Require additional authentication at startup: Allow BitLocker without a compatible TPM` to `Enabled: False`

  $adt_comp\BitLocker Drive Encryption\Operating System Drives\Require additional authentication at startup: Allow BitLocker without a compatible TPM

- [ ] Set `Require trusted path for credential entry` to `Enabled`

  $adt_comp\Credential User Interface\Require trusted path for credential entry

- [ ] Set `Allow Telemetry` to `Enabled: 0 - Security [Enterprise Only]`

  $adt_comp\Data Collection and Preview Builds\Allow Telemetry

- [ ] Set `Download Mode` to `Disabled`

  $adt_comp\Delivery Optimization\Download Mode

- [ ] Set `Application: Control Event Log behavior when the log file reaches its maximum size` to `Disabled`

  $adt_comp\Event Log Service\Application\Control Event Log behavior when the log file reaches its maximum size

- [ ] Set `Application: Specify the maximum log file size (KB)` to `Enabled: 32,768 or greater`

  $adt_comp\Event Log Service\Application\Specify the maximum log file size (KB)

- [ ] Set `Security: Control Event Log behavior when the log file reaches its maximum size` to `Disabled`

  $adt_comp\Event Log Service\Security\Control Event Log behavior when the log file reaches its maximum size

- [ ] Set `Security: Specify the maximum log file size (KB)` to `Enabled: 196,608 or greater`

  $adt_comp\Event Log Service\Security\Specify the maximum log file size (KB)

- [ ]  Set `Setup: Control Event Log behavior when the log file reaches its maximum size` to `Disabled`

  $adt_comp\Event Log Service\Setup\Control Event Log behavior when the log file reaches its maximum size

- [ ] Set `Setup: Specify the maximum log file size (KB)` to `Enabled: 32,768 or greater

  $adt_comp\Event Log Service\Setup\Specify the maximum log file size (KB)

- [ ] Set `System: Control Event Log behavior when the log file reaches its maximum size` to `Disabled`

  $adt_comp\Event Log Service\System\Control Event Log behavior when the log file reaches its maximum size

- [ ] Set `System: Specify the maximum log file size (KB)` to `Enabled: 32,768 or greater`

  $adt_comp\Event Log Service\System\Specify the maximum log file size (KB)

- [ ] Set `Configure Windows SmartScreen` to `Enabled: Require approval from an administrator before running downloaded unknown software`

  $adt_comp\File Explorer\Configure Windows SmartScreen

- [ ] Set `Turn off Data Execution Prevention for Explorer` to `Disabled`

  $adt_comp\File Explorer\Turn off Data Execution Prevention for Explorer

- [ ] Set `Turn off heap termination on corruption` to `Disabled`

  $adt_comp\File Explorer\Turn off heap termination on corruption

- [ ] Set `Turn off shell protocol protected mode` to `Disabled`

  $adt_comp\File Explorer\Turn off shell protocol protected mode

- [ ] Set `Prevent the computer from joining a homegroup` to `Enabled`

  $adt_comp\HomeGroup\Prevent the computer from joining a homegroup

- [ ] Set `Prevent the usage of OneDrive for file storage` to `Enabled`

  $adt_comp\OneDrive\Prevent the usage of OneDrive for file storage

- [ ] Set `Allow users to connect remotely by using Remote Desktop Services` to `Disabled`

  $adt_comp\Remote Desktop Services\Remote Desktop Session Host\Connections\Allow users to connect remotely by using Remote Desktop Services

- [ ] Set `Allow Cortana` to `Disabled`

  $adt_comp\Search\Allow Cortana

- [ ]  Set `Allow indexing of encrypted files` to `Disabled` 

  $adt_comp\Search\Allow indexing of encrypted files

- [ ] Set `Allow search and Cortana to use location` to `Disabled`

  $adt_comp\Search\Allow search and Cortana to use location

- [ ]  Set `Set what information is shared in Search` to `Enabled: Anonymous info`

  $adt_comp\Search\Set what information is shared in Search

- [ ] Set `Join Microsoft MAPS` to `Disabled`

  $adt_comp\Windows Defender\MAPS\Join Microsoft MAPS

- [ ] Set `Enables or disables Windows Game Recording and Broadcasting` to `Disabled`

  $adt_comp\Windows Game Recording and Broadcasting\Enables or disables Windows Game Recording and Broadcasting

- [ ] Set `Prevent Internet Explorer security prompt for Windows Installer scripts` to `Disabled`

  $adt_comp\Windows Installer\Prevent Internet Explorer security prompt for Windows Installer scripts

- [ ] Set `Configure Automatic Updates` to `Enabled`

  $adt_comp\Windows Update\Configure Automatic Updates

- [ ] Set `Turn off toast notifications on the lock screen` to `Enabled`

  User Configuration\Policies\Administrative Templates\Start Menu and Taskbar\Notifications\Turn off toast notifications on the lock screen

- [ ] Set `Turn off Help Experience Improvement Program` to `Enabled` 

  User Configuration\Policies\Administrative Templates\System\Internet Communication Management\Internet Communication Settings\Turn off Help Experience Improvement Program

- [ ] Set `Always install with elevated privileges` to `Disabled`

  User Configuration\Policies\Administrative Templates\Windows Components\Windows Installer\Always install with elevated privileges

Settings
========

System
------
Notification & actions
- [ ] Show me tips about Windows to `Off`
- [ ] Show notification on the lock to `Off`
- [ ] Show alarms, reminders, and incoming VoIP calls on the lock screen `Off`

Offline maps
- [ ] Automatically update maps to `Off`

Devices
-------
Typing
- [ ] Autocorrect misspelled words to `Off`

AutoPlay
- [ ] Use AutoPlay for all media and devices to `Off`

Network & Internet
------------------
Ethernet
- [ ] Change Adapter Options -> Disable File and Printer Sharing for Microsoft Networks & Disable NetBIOS (Advanced TCP/IP Settings)

Personalization
---------------
Start
- [ ] Occasionally show suggestions in Start to `Off`

Time & Language
---------------
Region & language
- [ ] Remove French

Privacy
-------
General
- [ ] Set everything to `Off` (except SmartScreen)

Location
- [ ] Set everything to `Off`

Camera
- [ ] Set everything to `Off`

Microphone
- [ ] Set everything to `Off`

Account Info
- [ ] Set everything to `Off`

Calendar
- [ ] Set everything to `Off`

Call History
- [ ] Set everything to `Off`

Email
- [ ] Set everything to `Off`

Messaging
- [ ] Set everything to `Off`

Radio
- [ ] Set everything to `Off`

Sync with devices
- [ ] Set everything to `Off`

Feedback & diagnostics
- [ ] Windows should ask for my feedback to `Never`

Background apps
- [ ] Set everything to `Off`

Update & Security
-----------------
Windows Update
- [ ] Choose how updates are delivered to `Off`

Windows Defender
- [ ] Cloud-based Protection to `Off`
- [ ] Automatic sample submission to `Off`

SMB v1
------
- [ ] Disable / Deinstall SMBv1

Office Hardening
----------------
- [ ] Set `Configure Attack surface reduction rules` to `Enabled`

  Windows components > Windows Defender Antivirus > Windows Defender Exploit Guard > Attack surface reduction

  Apply these rules (Set `Value` to `1` (Block Mode):
  ```
  BE9BA2D9-53EA-4CDC-84E5-9B1EEEE46550	Block executable content from email client and webmail
  D4F940AB-401B-4EFC-AADC-AD5F3C50688A	Block Office applications from creating child processes
  3B576869-A4EC-4529-8536-B80A7769E899	Block Office applications from creating executable content
  75668C1F-73B5-4CF0-BB93-3ECF5CB7CC84	Block Office applications from injecting into other processes
  D3E037E1-3EB8-44C8-A917-57927947596D	Impede JavaScript and VBScript to launch executables
  5BEB7EFE-FD9A-4556-801D-275E5FFC04CC	Block execution of potentially obfuscated scripts
  92E97FA1-2EDF-4476-BDD6-9DD0B4DDDC7B	Block Win32 imports from Macro code in Office	
  ```

- [ ] Apply Registry Settings

  [gist.githubusercontent.com/wdormann/disable_ddeauto.reg](https://gist.githubusercontent.com/wdormann/732bb88d9b5dd5a66c9f1e1498f31a1b/raw/69c9d9d14b386d8f178e59a046804501ec1ee304/disable_ddeauto.reg)

  Windows Registry Editor Version 5.00
  ```
  [HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Word\Options]
   "DontUpdateLinks"=dword:00000001
  
  [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Word\Options]
   "DontUpdateLinks"=dword:00000001
  
  [HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options]
   "DontUpdateLinks"=dword:00000001
  
  [HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Word\Options\WordMail]
   "DontUpdateLinks"=dword:00000001
  
  [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Word\Options\WordMail]
   "DontUpdateLinks"=dword:00000001
  
  [HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options\WordMail]
   "DontUpdateLinks"=dword:00000001
  
  [HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\OneNote\Options]
  "DisableEmbeddedFiles"=dword:00000001
  
  [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\OneNote\Options]
  "DisableEmbeddedFiles"=dword:00000001
  
  [HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Excel\Options]
   "DontUpdateLinks"=dword:00000001
   "DDEAllowed"=dword:00000000
   "DDECleaned"=dword:00000001
  
  [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Excel\Options]
   "DontUpdateLinks"=dword:00000001
   "DDEAllowed"=dword:00000000
   "DDECleaned"=dword:00000001
   "Options"=dword:00000117
  
  [HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Excel\Options]
   "DontUpdateLinks"=dword:00000001
   "DDEAllowed"=dword:00000000
   "DDECleaned"=dword:00000001
   "Options"=dword:00000117
  ```


