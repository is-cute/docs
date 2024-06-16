---
label: "ZeroTier"
icon: broadcast
order: -1
---

# ZeroTier

ZeroTier is a network service used to provide virtual private or public LAN solutions.

## Client

### Windows

==- :icon-download: Installing

- Download the Windows installer for [ZeroTier](https://www.zerotier.com/download) and launch the installer

[!button variant="primary" icon="download" text="MSI Installer (x86/x64)"](https://download.zerotier.com/dist/ZeroTier%20One.msi)

- Once installed, go to your system tray and locate ZeroTier. Right-click on the icon > **Join New Network...**

![Opening ZeroTier](/static/other/zerotier/client/windows-installing.gif)

==- :icon-globe: Connecting to Networks

- Enter the unique 16-digit network ID set up by you or provided by the administrator into the box and click **Join**. The network should show up in the ZeroTier UI
  - *Private networks will not show up on your client until it is approved.* [Manage your network](https://my.zerotier.com) or contact the network administrator

![Connecting to a network](/static/other/zerotier/client/windows-connecting.gif)

==- :icon-unlink: Leaving Networks

- Right-click on the ZeroTier UI icon. Then, hover over the network you wish to disconnect from > **Disconnect**

![Leaving a network](/static/other/zerotier/client/windows-leaving.gif)

==- :icon-trash: Uninstalling

- Open Control Panel and navigate to **Programs** > **Programs & Features** > **Uninstall a program**
- Select ZeroTier from the program list and click **Uninstall**. Follow the on-screen instructions to remove ZeroTier

![Uninstalling ZeroTier](/static/other/zerotier/client/windows-uninstalling.gif)

===

### Arch

==- :icon-download: Installing

- Download the [Arch package](https://archlinux.org/packages/extra/x86_64/zerotier-one) for [ZeroTier](https://www.zerotier.com/download) through terminal using `pacman`

```bash
sudo pacman -S zerotier-one
```

![Installing ZeroTier using terminal](/static/other/zerotier/client/linux-installing.gif)

- Start the `zerotier-one` service:
  - *You may need to start it in order to connect to a network*

```bash
sudo systemctl start zerotier-one
```

- Alternatively, you can choose to have the service run on system startup:

```bash
sudo systemctl enable zerotier-one
```

![Enabling the ZeroTier service](/static/other/zerotier/client/linux-installing2.gif)

==- :icon-globe: Connecting to Networks

- Connect to a ZeroTier network using terminal, replacing `<network_ID>` with the unique 16-digit network ID set up by you or provided by the administrator

```bash
sudo zerotier-cli join <network_ID>
```

- Check that you are connected to a network. If successful, the network will show up
  - *Private networks will not show up on your client until it is approved.* [Manage your network](https://my.zerotier.com/) or contact the network administrator

```bash
sudo zerotier-cli listnetworks
```

![Connecting to a Network](/static/other/zerotier/client/linux-connecting.gif)

==- :icon-unlink: Leaving Networks

- Leave a ZeroTier network using terminal, replacing `<network_ID>` with the unique 16-digit network ID you wish to disconnect from

```bash
sudo zerotier-cli leave <network_ID>
```

![Leaving a Network](/static/other/zerotier/client/linux-leaving.gif)

==- :icon-trash: Uninstalling

- Uninstall the Arch package for Zerotier using `pacman`:

```bash
sudo pacman -R zerotier-one
```

===

### Debian

==- :icon-download: Installing

- Download [ZeroTier](https://www.zerotier.com/download) using the SSL-based install script:

```bash
curl -s https://install.zerotier.com | sudo bash
```

- Start the `zerotier-one` service:
  - *You may need to start it in order to connect to a network*

```bash
sudo systemctl start zerotier-one
```

- Alternatively, you can choose to have the service run on system startup:

```bash
sudo systemctl enable zerotier-one
```

==- :icon-globe: Connecting Networks

- Connect to a ZeroTier network using terminal, replacing `<network_ID>` with the unique 16-digit network ID set up by you or provided by the administrator

```bash
sudo zerotier-cli join <network_ID>
```

- Check that you are connected to a network. If successful, the network will show up
  - *Private networks will not show up on your client until it is approved.* [Manage your network](https://my.zerotier.com/) or contact the network administrator

```bash
sudo zerotier-cli listnetworks
```

==- :icon-unlink: Leaving Networks

- Leave a ZeroTier network using terminal, replacing `<network_ID>` with the unique 16-digit network ID you wish to disconnect from

```bash
sudo zerotier-cli leave <network_ID>
```

==- :icon-trash: Uninstalling

- Uninstall the package for Zerotier using `apt`:

```bash
sudo apt remove zerotier-one
```

===

## Server

ZeroTier can be used to host various services over their network, such as a multiplayer game over LAN or a web server. This section details additional information that may be useful for hosting.

!!!info
See [Troubleshooting & FAQ](https://docs.zerotier.com/zerotier/troubleshooting) on the official ZeroTier docs.
!!!

### Windows

==- Setting the Firewall Rule Group

In Windows, connected networks are categorized by *Private* or *Public* to determine firewall rules to use. If your ZeroTier interface shows up as a *Public network*, you may need to set it to *Private* to allow client connections.

- Launch a [Windows Powershell](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/powershell) window as Administrator
- Locate the `Name` for your ZeroTier network adapter using `Get-NetConnectionProfile`. *You should see `ZeroTier One [xxxxxxxxxxxxxxxx]` listed under `Interface Alias`*

![Checking ZeroTier's network adapter](/static/other/zerotier/server/windows-firewall.png)

- Set the ZeroTier network interface to *Private*, replacing `<interface_name>` with the name of your network interface:

```bash
Set-NetConnectionProfile -Name "<interface_name>" -NetworkCategory Private
```

![Setting ZeroTier's network adapter](/static/other/zerotier/server/windows-firewall2.png)

==- Allowing Pings to Your Host

In Windows, the built-in firewall blocks pings to your host by default, preventing clients from pinging your server.

Enabling these firewall rules typically isn't required by your host. *However, if you encounter problems with inbound connections, it may help for troubleshooting.*

!!!warning Warning
While disabling your firewall may allow pings, *it is not recommended as it can leave your server at risk*
!!!

- On your host, launch [Windows Defender Firewall with Advanced Security](https://learn.microsoft.com/en-us/windows/security/operating-system-security/network-security/windows-firewall/windows-firewall-with-advanced-security)
- Under ***Inbound Rules***, enable all rules titled ***File and Printer Sharing (Echo Request - ICMPv4-In)***.

![Allowing pings to your host](/static/other/zerotier/server/windows-pings.gif)

===

===
