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
Client:
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```
Server:
```

import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT
![image](https://github.com/hamza9559/3b_CHAT_USING_TCP_SOCKETS/assets/154586530/d5df9f2c-f15e-41c1-b2ed-754ded8dd501)
![image](https://github.com/hamza9559/3b_CHAT_USING_TCP_SOCKETS/assets/154586530/56ba345f-d693-4360-868c-c1339a72c7e1)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
