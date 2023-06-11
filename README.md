# EX-4 : IMPLEMENTATION OF ADDRESS RESOLUTION PROTOCOL (ARP)
## DATE : 30-03-2023
## AIM :
To write a python program for simulating ARP protocols using TCP.

## ALGORITHM :
- Start the program
- Accept the socket which is created by the client.
- Server maintains the table in which IP and corresponding MAC addresses are stored.
- Read the IP address which is send by the client.
- Map the IP address with its MAC address and return the MAC address to client.

## PROGRAM :
### CLIENT :
```
## Developed : MIDHUN AZHAHU RAJA P
## Reg no : 212222240066


 # Developed By : kishore.S
 # Register Number : 22008388
import socket
s=socket.socket()
s.bind(('localhost',8000))
@@ -31,15 +32,17 @@ while True:
        c.send(address[ip].encode())
    except KeyError:
        c.send("Not Found".encode())
 ```
### SERVER :

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    ip=input("Enter logical Address : ")
    s.send(ip.encode())
    print("MAC Address",s.recv(1024).decode())
```
## OUTPUT :
### SERVER OUTPUT :
![image](https://github.com/Kishore2o/EX-4/assets/118679883/ab8a39e8-0070-4d99-bb03-948aaf4ea352)

## RESULT :
Thus, the python program for simulating ARP protocols using TCP was successfully executed.

