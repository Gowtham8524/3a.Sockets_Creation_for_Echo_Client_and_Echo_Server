# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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
```py
Client
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
```py
Server
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUPUT
client
![client](https://github.com/user-attachments/assets/f31e02f0-1279-4469-b3df-e38adb78c97f)
server
![server](https://github.com/user-attachments/assets/9fafa5e0-78d0-413f-a982-47af4a63f400)



## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
as successfully created and executed.
