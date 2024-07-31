# SEE wireshark-intro.pdf lab manual for specific objective details for the solutions below
For this lab, I analyzed a .pcap file inside of wireshark to locate TELNET packets which contains login attempts for a user 'john'. The objective was to locate the password that was used during the login attempt and 
save the packet to a new pcap file. 

## 3.3 Find a specfic packet

To find the specific packet more efficiently, I applied a display filter (telnet.data) within wireshark to narrow the traffic to just the TELNET protocol.
Once the traffic was filtered, the invalid password was identified and saved to separate pcap file named 'invalidpassword.pcap'


## 3.4 Explore some more
Diving deeper into the attempted login attempts for the user 'john' over TELNET, I was able to view the full session using the Analyze->Follow->TCP function in Wireshark to view the full details of the TELNET session traffic:

