# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
DEVELOPED BY:ATCHAYA.K


REGISTER NUM:212223220011

SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

## OUTPUT:
![image](https://github.com/Atchayakunchithapatham/3b_CHAT_USING_TCP_SOCKETS/assets/144870744/38660134-ec2d-4363-b77c-13e5a16da4f3)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
