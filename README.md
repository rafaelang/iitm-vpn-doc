# IITM VPN Documentation
IIT Madras provides VPN access to its netowrk via Fortigate SSL VPN. 
In order to enable VPN, student/faculty/staff should make a request to Computer Center.
VPN can be accessed through FortiClient by using LDAP username and password.

## Installation

### Windows, MacOS, iOS & Android

- Download and install `Forticlient` from 
  [FortiNet Website](https://www.fortinet.com/support-and-training/support/product-downloads.html)
- `FortiClient` is also available for download at [IITM Website](https://vpn.iitm.ac.in:10443) (Login using LDAP)
- Direct download links:
  - [Windows](http://forticlient.com/downloads/FortiClientOnlineInstaller.exe)
  - [Windows 10 Universal App](https://www.microsoft.com/en-ca/store/p/forticlient/9wzdncrdh6mc)
  - [MacOS](http://forticlient.com/downloads/FortiClient_Installer.dmg)
  - [iOS](http://itunes.apple.com/md/app/forticlient/id525600370?mt=8)
  - [Android](https://play.google.com/store/apps/details?id=com.fortinet.forticlient)

### Ubuntu & Debian

- Download and install `OpenFortiGUI` from
  [Bits and Bytes](https://hadler.me/linux/openfortigui/)
- Direct download links:
  - [Ubuntu 16.04 64 bit](https://hadler.me/files/openfortigui/openfortigui_0.2.10-1_amd64.deb) 
  - [Ubuntu 16.04 32 bit](https://hadler.me/files/openfortigui/openfortigui_0.2.10-1_i386.deb)
  - [Debian 9 64 bit](https://hadler.me/files/openfortigui/openfortigui_0.2.10-1_amd64_debian9.deb)

### Other Linux

- Build `OpenFortiGUI` from source: [Instructions](https://hadler.me/linux/openfortigui/)
- Use `OpenFortiVPN` from command line: [Instructions](https://github.com/adrienverge/openfortivpn)

## Usage

### Windows, MacOS, iOS & Android

- Launch FortiClient
- Create a new VPN profile with following parameters:
  - Name: `IITM`
  - Type: `SSL VPN`
  - Server: `vpn.iitm.ac.in`
  - Port: `10443`
  - Username: `<your-ldap-username>`
  - Password: `<your-ldap-password>`
- Save the profile and connect
- You can now use any browser to get IITM interNal websites

#### Windows
![FortiClient on Windows](forticlient_windows_connect.gif)

#### Android
![FortiClient on Android](forticlient_android_connect_opt.gif)

### Linux (OpenFortiGUI)

- Launch `OpenFortiGUI`
- Click `Add -> VPN`
- Enter the following details:
  - Name: `IITM`
  - VPN-Server: `vpn.iitm.ac.in`
  - VPN-Port: `10443`
  - Username: `<your-ldap-username>`
  - Password: `<your-ldap-password>`
- Click `Save`
- Select `IITM` from the list of VPNs
- Click `Connect` button on top

![OpenFortiGUI on Ubuntu](openfortigui.gif)
