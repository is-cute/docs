---
label: "ZeroTier"
icon: broadcast
order: -1
---

# ZeroTier

ZeroTier is a network service used to provide virtual private or public LAN solutions.

## Windows
==- Installing
- Download the Windows installer for [ZeroTier](https://www.zerotier.com/download) and launch the installer.

[!button variant="primary" text="MSI Installer (x86/x64)"](https://download.zerotier.com/dist/ZeroTier%20One.msi)

- Once installed, go to your system tray and locate ZeroTier. Right-click on the icon > ***Join New Network...***.

![](/static/other/zerotier/windows-installing.gif)

==- Connecting
- Enter the unique 16-digit network ID set up by you or provided by the administrator into the box and click **Join**. The network should show up in the ZeroTier UI.
   - *Private networks will not show up on your client until it is approved.* [Manage your network](https://my.zerotier.com/) or contact the network administrator.

![](/static/other/zerotier/windows-connecting.gif)

==- Leaving
- Right-click on the ZeroTier UI icon. Then, hover over the network you wish to disconnect from > ***Disconnect***.

![](/static/other/zerotier/windows-leaving.gif)

===

## Arch

==- Installing
- Download the [Arch package](https://archlinux.org/packages/extra/x86_64/zerotier-one) for [ZeroTier](https://www.zerotier.com/download) through terminal using `pacman`.
```
sudo pacman -S zerotier-one
```

![](/static/other/zerotier/linux-installing.gif)

- Start the `zerotier-one` service:
   - *You may need to start it in order to connect to a network.*
```
sudo systemctl start zerotier-one
```
- Alternatively, you can choose to have the service run on system startup:
```
sudo systemctl enable zerotier-one
```

![](/static/other/zerotier/linux-installing2.gif)

==- Connecting
- Connect to a ZeroTier network using terminal, replacing `<network_ID>` with the unique 16-digit network ID set up by you or provided by the administrator.
```
sudo zerotier-cli join <network_ID>
```
- Check that you are connected to a network. If successful, the network will show up.
   - *Private networks will not show up on your client until it is approved.* [Manage your network](https://my.zerotier.com/) or contact the network administrator.
```
sudo zerotier-cli listnetworks
```

![](/static/other/zerotier/linux-connecting.gif)

==- Leaving
- Leave a ZeroTier network using terminal, replacing `<network_ID>` with the unique 16-digit network ID you wish to disconnect from.
```
sudo zerotier-cli leave <network_ID
```

![](/static/other/zerotier/linux-leaving.gif)

===

## Ubuntu/Debian (DEB/RPM)

==- Installing
- Download [ZeroTier](https://www.zerotier.com/download) using the SSL-based install script:
```
curl -s https://install.zerotier.com | sudo bash
```

- Start the `zerotier-one` service:
   - *You may need to start it in order to connect to a network.*
```
sudo systemctl start zerotier-one
```
- Alternatively, you can choose to have the service run on system startup:
```
sudo systemctl enable zerotier-one
```

==- Connecting
- Connect to a ZeroTier network using terminal, replacing `<network_ID>` with the unique 16-digit network ID set up by you or provided by the administrator.
```
sudo zerotier-cli join <network_ID>
```
- Check that you are connected to a network. If successful, the network will show up.
   - *Private networks will not show up on your client until it is approved.* [Manage your network](https://my.zerotier.com/) or contact the network administrator.
```
sudo zerotier-cli listnetworks
```

==- Leaving
- Leave a ZeroTier network using terminal, replacing `<network_ID>` with the unique 16-digit network ID you wish to disconnect from.
```
sudo zerotier-cli leave <network_ID
```

===