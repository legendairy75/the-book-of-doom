# Server IP Address Issue

TL:DR

1. tried connecting to server
2. server had wrong ip
3. loged into router and changed servers ip
4. rebooted server but still wrong ip
5. did what chat said to do, didnt work
6. mac changes, ip stays the same (27)
7. login web with wrong ip
8. find bridge settings and fix ipv4 to right ip
9. rebooted and problem salved

Logged into my pc this morning to connect to my server & start my containers (they should auto start but I havent set that up yet) only to find that the local domain name dosnt work, well thats expected scence the pi hole container hasnt started yet. so i try the ip address, still nothing; this is a problem becaus the server should be fixed to that address.

So I log into the server directly and use `ip a` to check and sure enough it was the wrong address.