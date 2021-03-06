## Inspiration
The inspiration for this project came from Ephemeral2 (http://ephemeralp2p.durazo.us/2bbbf21959178ef2f935e90fc60e5b6e368d27514fe305ca7dcecc32c0134838)

Ephemeral is a webpage that does not live on a conventional server; instead, it is hosted by the clients that visit it, making it decentralized/distributed/P2P.

I wanted to learn how to build something similar, such as a P2P, self-hosted chat room. At the same time, I always wanted to try building a captive portal and since Cisco was promoting the Meraki platform, I decided to combine the two ideas. Introducing: EmergencyChat!

## What it does
EmergencyChat is a P2P chatroom that lives on a Wi-Fi network. The Wi-Fi network is created by Cisco’s Meraki platform (both hardware and software). The idea is to deploy this system during a natural calamity, such as the recent Hurricane Irma in Puerto Rico, which heavily disrupted the Internet on the island. Once the network is set up, only registered users (RADIUS authentication) can access the Internet, while everyone can communicate through the chatroom. In such an occurrence, the Internet link is often slower and expensive: that's why it is critical to restrict its access to emergency personnel only, while at the same time allowing everyone to receive updates (through the network-wide chatroom).

## How I built it
I used Vanilla JS and WebSockets for the chatroom, NodeJS/Express/Mongo for the Captive Portal. Cisco Meraki for the cloud management of the network.

## Challenges I ran into
Setting up the Captive Portal was tricky because I had never used the technology before. I was eventually able to get it to work thanks to Matt DeNapoli (Cisco) who helped me out. Also, the final product doesn’t look pretty and it doesn’t have as much functionality as I’d want. Unfortunately, working solo meant that I couldn’t develop it as much.

## Accomplishments that I'm proud of
I’m very happy of my time management, the idea creation and the final result, even though it’s not as complete as I would desire.

## What I learned
Implementing WebSockets; Cisco’s Meraki platform and setting up a captive portal from scratch.

## What's next for EmergencyChat
Right now, the application works even when the Internet goes down (making it a reliable way to communicate during potential channel disruptions); however, it’s not truly ephemeral/P2P as the local server hosting the WebSocket connector has to be reachable on the network. In future development, I want to implement zero point of failure communication (probably using webRTC).
