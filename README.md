# Cisco Meraki ExCap Splash Page Server

Overview

This Node.JS applications provides an example of the ExCAP interface for delivering a custom Captive Portal / Splash Page for Cisco Meraki access points.

More info about the ExCap API: https://meraki.cisco.com/lib/pdf/meraki_whitepaper_captive_portal.pdf

#Usage

Configure the Wi-Fi SSID

Logon to the Meraki Dashboard

Dashboard --> Wireless --> Access Control: (select SSID name from list)

Configure an SSID with a Sign-on or Click-through splash page.

Scroll down the page and enable the "Walled Garden". Enter the IP address of your web server, to provide access to your splash page content prior to authentication. Enter any additional IP addresses for hosted content such as images, terms of service, etc in this section as well.

Configure the Splash Page

Dashboard --> Wireless --> Configure --> Splash Page Select: Use custom URL

Enter the URL for the splash page. This flow provides two options, Sign-on and Click-through.

#Sign-on

http://yourserver/signon


#Click-through

http://yourserver/click


#Run


Clone the app

npm install

run app.js
   (ideally with pm2..   pm2 start app.js --name excap )

#Report
You can see the session data by going to

http://yourserver/excapData/excap

#Enjoy!

Note: You should run this using SSL. The reports are not protected in anyway, so either sort that out or disable the mongodb REST route.


#More Details and other projects
www.InternetOfLego.com

