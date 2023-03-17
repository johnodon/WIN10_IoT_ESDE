Insall IOT Enterprise
Install all updates
Create local account
Enable remote desktop

Activate
Powershell (non-admin)
irm https://massgrave.dev/get | iex

Hide elements, change shell, enable SMB1
Turn Windows features on or off
+Device Lockdown
custom boot, unbranded boot, shell launcher 
+SMB 1.0/CIFS File Sharing Support
automatic removal, client, server

All network browsing to unraid
gpedit
Local computer policy --> Computer configuration --> Administrative Templates -->
Network --> Lanman Workstation
Enable insecure guest logons = 1

re-enable checkbox for netplwiz
Powershell as admin
reg ADD “HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\PasswordLess\Device” /v DevicePasswordLessBuildVersion /t REG_DWORD /d 0 /f

unbranded boot
cmd as admin
bcdedit.exe -set {globalsettings} bootuxdisabled on

Hide autologon ui
regedit
Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Embedded\EmbeddedLogon
HideAutoLogonUI = 1
HideFirstLogonAnimation = 1

chnage shell to ES-DE
Regedit
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon
Shell = path to esde exe

Connect DS4 controllers via BT
Install DS4Windows and HIDHide
Allow DS4W in HidHide
Launch DS4W with admin
Settings
Start at logon as task
Start minimized
Closes minimizes
