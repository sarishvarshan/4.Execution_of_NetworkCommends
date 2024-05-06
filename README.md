# 4.Execution_of_NetworkCommands
### Developed by: Sarish Varshan V
### Register Number: 212223230196
## AIM 
Use of Network commands in Real Time environment
## Software 
Command Prompt And Network Protocol Analyzer
## Procedure
## To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## Program
### PING COMMAND
### CLIENT
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```
### SERVER
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```
### Trace Route Command
```
from scapy.all import* 
target = ["www.google.com"] 
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```
## Output
### PING COMMAND
### CLIENT
![318509110-d4012c35-9f3a-48a4-8338-01a03a0bf810](https://github.com/sarishvarshan/4.Execution_of_NetworkCommends/assets/152167665/929fcf11-6d2d-4a9a-99eb-a5c7400bfe03)
### SERVER
![318509220-41a703f5-1cd5-42fe-a821-d1533f4820ef](https://github.com/sarishvarshan/4.Execution_of_NetworkCommends/assets/152167665/30070126-2a26-4401-9099-762385eefc97)
### TRACE ROUTE COMMAND
![318509371-ed1e8d7d-22d4-400f-b102-fefe2c182e45](https://github.com/sarishvarshan/4.Execution_of_NetworkCommends/assets/152167665/a8131a51-3cad-40ae-bfff-f7fb4a5e4aa9)




## Result
Thus Execution of Network commands Performed 
