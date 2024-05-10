# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

## Developed by : Preethi S
## Register no: 212223230157

# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
## SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
 ```
 ## CLIENT
 ```
 import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
## OUPUT

![image](https://github.com/PreethiS647/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147313372/26fffb56-5f91-45fb-a66a-fb0ba2a5af1f)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
