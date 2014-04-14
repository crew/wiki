Trusting SSL on the Crew Network
================================

In order to get your computer to trust the Crew SSL certificates you need to install the Crew Certificate Authority’s Root Certificate into your Certificate store.  This is not necessary for normal usage of the crew network, just a convenience to stop your computer from constantly whining about certificate errors

Mac
---

1. Go to [foreman](foreman.crew.ccs.neu.edu) using Google Chrome (ignore certificate warning)
2. Click the red lock with an x on it and switch to the ***connection*** tab
3. Click on ***Certificate Information*** link
4. Select on the Puppet CA: foreman.crew.ccs.neu.edu
5. Drag the image of the Certificate (the bigger one next to the text ‘Expires:…’ ) to your desktop
6. Open ***Keychain Access***
7. Go to the ***System*** Keychain 
8. Click the ***+*** button in the System Keychain and browse to the Puppet CA Root Certificate on your desktop
9. Enter Your password
10. Reboot


