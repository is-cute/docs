---
label: "Joining a Server"
icon: globe
order: -1
---

# Joining a Server

Instructions on how to join multiplayer servers in *Minecraft: Java Edition*.

!!!info
*You may need to setup ZeroTier in order to join certain servers.* See how to join in [ZeroTier](/other/zerotier.md).
!!!

## Connecting

- Launch Minecraft, then go to **Multiplayer** > **Add Server** or **Direct Connect**
- Under **Server Address**, paste your server IP or the IP provided by the administrator and click **Done**
  - If configured properly, your client will ping the server and the server's MOTD will show up. *If it does not show up, ensure the server is running and that you've inputted the correct address*

![Connecting to a multiplayer Minecraft server](/static/minecraft/joining/connecting.gif)

!!!warning Warning
Cracked clients can only play on servers that are in offline mode. *Servers running in online mode require official accounts to properly authenticate with Mojang servers.*
!!!

## Troubleshooting

If you are unable to join, confirm you have verified all of the following:

- The server is active and running
- The correct Minecraft version and modpack (if applicable)
- You have installed [additional or updated mods](/minecraft/curseforge.md#downloading-extra-mods) required by the server
- You have an official or cracked Minecraft account
- Proper [ZeroTier network configuration](/other/zerotier.md)
