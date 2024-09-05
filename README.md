# How to open CSGO server over internet without GSLT or fix for LAN servers are restricted to local clients (class C)

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
Available soon
