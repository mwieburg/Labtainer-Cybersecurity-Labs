# SEE wireshark-intro.pdf lab manual for specific objective details for the solutions below
For this lab, I analyzed a .pcap file inside of wireshark to locate TELNET packets which contains login attempts for a user 'john'. The objective was to locate the password that was used during the login attempt and 
save the packet to a new pcap file. 

## 3.3 Find a specfic packet

To find the specific packet more efficiently, I applied a display filter (telnet.data) within wireshark to narrow the traffic to just the TELNET protocol.
Once the traffic was filtered, the invalid password was identified and saved to separate pcap file named 'invalidpassword.pcap'

![ws_telnet_filter](https://github.com/user-attachments/assets/92acfc49-fabc-4d57-8607-dca1040d86e8)

Invalid password packet identified

![ws_telnet_john_password](https://github.com/user-attachments/assets/85ed8ffd-b977-4d57-adf5-444b08ae3206)

Invalid password packet identified saved to seperate pcap file

![ws_telnet_invalidpassword_pcap](https://github.com/user-attachments/assets/d2654dc0-f8ab-41eb-908f-5d802e9d5ce5)

## 3.4 Explore some more
Diving deeper into the attempted login attempts for the user 'john' over TELNET, I was able to view the full session using the Analyze->Follow->TCP function in Wireshark to view the full details of the TELNET session traffic:

![ws_explore_some_more](https://github.com/user-attachments/assets/30acdc1f-7d52-4060-bf90-7f7bf57b9d61)
