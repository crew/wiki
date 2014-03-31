Logging Into Crew Remotely 
===========================

If you want to get work done remotely then here is how you login to the crew
network.  Note that this will change with v2 of the Crew Network which will be
built soon

Mac
---

We are going to use a SOCKS proxy to proxy all your traffic though to the crew
network.  This is similar to a VPN but instead of using a VPN Client we are
using SSH.

[^]: **Automatic Connection**



To automatically connect and disconnect the SOCKS proxy use this script



`#!/bin/bash`

`networksetup -setsocksfirewallproxystate Wi-Fi on`

`ssh -D <rand int 8000 - 65535> <ccis username>@alpha.ccs.neu.edu`

`networksetup -setsocksfirewallproxystate Wi-Fi off`



You can place it in you home directory (~) and name it something like crew.sh

Make it executable `chmod +x ~/crew.sh`



To connect: `sudo ~/crew.sh`



The benefit of this method is that it will automatically disable the SOCKS proxy
if the SSH tunnel dies (you closed your computer without logging out)



**Also**

-   I would add my ssh key to Alpha so that I don’t have to enter my password
    each time and so that you are more secure then run `sudo cp -r /Users/<local
    user account>/.ssh /var/root/.ssh`

-   You can also add crew.sh to your PATH but I will leave that up to you

-   You can also modify your sudo config to not require a password for the crew
    script





[^]: **Manual Connection**

To connect manually open terminal and type the following command replacing the
bracketed text with your info:

`ssh -D <rand int 8000 - 65535> <ccis username>@alpha.ccs.neu.edu`

For example I enter: `ssh -D 56463 hurtige@alpha.ccs.neu.edu`



Then go to System Preferences \> Network \> (You active internet connection)



Click the `Advanced` button then go to the `Proxies` Tab



Check `SOCKS Proxy` and enter `localhost` and the poert number in the two boxes
under `SOCKS Proxy Server`



Click `OK` then `Apply`



You are now tunneling all your traffic through ALPHA and you can access
everything in the crew network.



