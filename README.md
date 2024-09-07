# How to open CSGO server over internet without GSLT or fix for "LAN servers are restricted to local clients (class C)"

Currently confirmed to work on CSGO no Steam version 2018-01-10 (Windows version)

**WARNING:** I don't know if you can get VAC banned for using this, but **USE AS YOUR OWN RISK!!!**

## TL;DR
- Find `engine.dll` (or something like that). It's usually in `Counter Strike Global Offensive\bin\engine.dll`
- Use a hex editor (like HxD) and open that file
- Find the hex string `72 03 B0 01 C3 32 C0 C3` and replace it with `72 03 B0 01 C3 B0 01 C3`
- Find the hex string `FF D0 84 C0 8B 07 75 1B` and replace it with `FF D0 84 C0 8B 07 EB 1B`
- Launch your dedicated server or your CS:GO game with `+sv_lan 1 +ip 0.0.0.0` in the launch option
- Expose/Open your port 27015 to the Internet (router specific, but usually a setting you can find in 192.168.1.1)
- Send the patched DLL to your friend
- Tell him to connect to your server using console and the command `connect`
- Enjoy!

## Details?
Normally, you have two option for openning a multi-player CS:GO server: either LAN-only server (only people on the same LAN network as yours) or internet server (people outside your LAN can connect). But the internet server would require [Game Server Login Token](https://steamcommunity.com/dev/managegameservers) passed to its parameter, or else they will fallback to LAN server. This is implemented by Valve to restrict things like skin-modding or prohibited plugins, and Valve will regularly scan servers with the token and ban violated servers.

Easy right? Just get a GSLT! No way. You must meet these conditions to be able to get a GSLT:

> - Your Steam account must not be currently community banned or locked.
> - Your Steam account must not be limited.
> - Your Steam account must have a qualifying registered phone.
> - Your Steam account must own the game for which you are creating a game server account.
> - Your Steam account may create 1000 game server accounts.

And if for some reasons you can't meet, you won't be able to get a token. For example, you need to pay at least $5 to be considered "not limited", and that's why I'm creating this guide.

So, without the token, when you try to connect to the server from outside your LAN, you will get this:

![image](https://github.com/user-attachments/assets/64138fea-ebec-4a9c-b66b-a54157dda0f1)

(to be added soon)
