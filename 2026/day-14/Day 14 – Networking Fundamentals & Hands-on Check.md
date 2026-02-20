# Day 14 – Networking Fundamentals & Hands-on Check

# Task:1 

Map the OSI vs TCP/IP models in your own words

Run essential connectivity commands

Capture a mini network check for a target host/service

## OSI MODEL 
- There are seven layer in OSI MODEL.

- Application layer:    user interphase like broswer,gmail,yoitube etc.
 
- presention layer:   Date encryption,decryption,formates the data,it handles compression.
  
- Session layer   :   established the connection between senderr and receiver like whatsapp session.
 
- Transport layer :   ensure data end-to-end datad delivery.use tcp for reliable delivery.use udp fro fast delivery.
 
- Network layer   :    Handles logical addressing and routing.Use ip naddress andchoose best path for data sending.
  
- Data link layer :   Responsible for use mac address,performs error detection,creat data frames.
 
- Physical layer  :   Responsible for physical data transmission.send data as bits using cables,wireless signals etc.

 # Task:2  TCP/IP MODEL

- There are four layers;
- Application layer :  Combination of OSI apllication layer+presention layer+session layer using protoclos like DNS,DHCP,HTTP,HTTPS,FTP,SMTP,SNMP,etc

- Transport layer : same as osi transp0ort layer.using TCP/UDP

- Internet layer  : same as osi internet layer

- Network layers  : Physical +data link layer

- ### prtoclos placement
- Application layer : DNS,DHCP,HTTP,HTTPS,FTP,TFTP,SMTP,SNMP.

- Transport layer   : TCP/UDP  TCP:it is responsible for segement pf data packets,retransmission packets,non realtime,and udp is responsible for real time data like zoom meetings,live calls,and no retransmission of data packets

- Internet layer : IP,ARP,ICMP

- Netwokr access layer : ethernet,wifi

  # Practical example
  - curl https://trainwithshubham.com
  - how TCP/IP works
  - step:1 APPLICATION LAYER
   
  - curl creates HTTPS request
    
    - STEP:2 TRANSPORT LAYERS:
    - 
    - A TCP connection is established .TCP performs a  3-way handshake
   
    - STEP:3 INTERNET LAYER: Protoclos ip ,add source & destination ip
   
    - STEP:5  DATA LINK LAYER
    
    - frame created.send through ethernet/wifi
   
    - ### 
   One real example: “curl https://example.com = App layer over TCP over IP”
    - <img width="1366" height="768" alt="Screenshot (236)" src="https://github.com/user-attachments/assets/ce2ccf05-317e-4deb-8738-58e1990afc56" />

# Hands-on Checklist   (run these; add 1–2 line observations

- Identity: hostname -I (or ip addr show) — note your IP

- <img width="1366" height="768" alt="Screenshot (237)" src="https://github.com/user-attachments/assets/e377656b-5200-4c39-b937-d9bf475e891e" />

- Observation:  my ip adress is 172-31-19-236

## Reachability: ping <target> — mention latency and packet loss.

- i ping trainwithshubham.com

- <img width="1366" height="768" alt="Screenshot (239)" src="https://github.com/user-attachments/assets/e237c1ef-1ea4-486a-ba89-74efd224aaa0" />

- Observation: 9 packets transmitted and 9 receiver . 0 packets loss and latency time is 8188ms. 

- ##  Path: traceroute <target> (or tracepath) — note any long hops/timeouts.

- ??????

- ## orts: ss -tulpn (or netstat -tulpn) — list one listening service and its port.net

- <img width="1366" height="768" alt="Screenshot (240)" src="https://github.com/user-attachments/assets/7d66489b-411b-4631-8e33-59ef4ecf7f68" />

-Observation: port is 22 and service name is sshd

## Name resolution: dig <domain> or nslookup <domain> — record the resolved IP.
- dig www.google.com
- Observation: we got 4 different resloved ip
  
<img width="1366" height="768" alt="Screenshot (242)" src="https://github.com/user-attachments/assets/869e1d05-7ab2-46e4-b153-c98976aa1c80" />

- ## Connections snapshot

- <img width="1366" height="768" alt="Screenshot (244)" src="https://github.com/user-attachments/assets/0e4a6458-b6a9-486c-998d-f82ff72bb300" />


## HTTP check: curl -I <http/https-url> — note the HTTP status code

# Mini Task: Port Probe & Interpret
- Identify one listening port from ss -tulpn (e.g., SSH on 22 or a local web app).

- <img width="1366" height="768" alt="Screenshot (245)" src="https://github.com/user-attachments/assets/f32e2858-ef05-49f3-821b-81d0de4c2490" />
## From the same machine, test it: nc -zv localhost <port> (or curl -I http://localhost:<port>).

<img width="1366" height="768" alt="Screenshot (246)" src="https://github.com/user-attachments/assets/4156af17-06b9-4dc9-a256-9df402922a2c" />
- connection succeeded.
