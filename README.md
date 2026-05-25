# s60v3-tether-ppp
Bluetooth tethering of s60v3 phones in Debian 13 (trixie) using ppp rather than wvdial

Tethering means sharing the internet connection in your phone with your computer 

Put "chatscript-provider" in /etc/chatscripts/ and replace "apn.provider.com" with the APN of your mobile phone provider

Put "peers-provider" in /etc/ppp/peers/

Put the s60v3-tether script in ~/bin or some other directory in the path, and make it executable (chmod +x s60v3-tether-ppp)

Put yourself in the sudoers group: e.g. for user john: "usermod -aG sudo john" (for this to be effective you need to log out and log in again)

Pair your phone with your computer; set the computer as "authorised" in the bluetooth menu of the phone

Run "s60v3-tether phone_name" in a terminal to tether the phone with bluetooth name "phone_name"

Ctrl-C stops the tethering session leaving the system consistent (both during dial-up channel search or during wvdial)

Note: for the Evolution email client to work during tethering, set "Method to detect online state" to "base" in "Settings>Network Preferences" 
