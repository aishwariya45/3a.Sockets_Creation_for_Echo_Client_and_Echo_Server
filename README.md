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
client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8002)) 
while True: 
     msg=input("Client > ") 
     s.send(msg.encode()) 
     print("Server > ",s.recv(1024).decode())


```
server
```
import socket 
s=socket.socket() 
s.bind(('localhost',8002)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
             ClientMessage=c.recv(1024).decode() 
             print("Client > ",ClientMessage) 
             msg=input("Server > ") 
             c.send(msg.encode()) 

```
## OUPUT
![Screenshot 2025-05-21 123035](https://github.com/user-attachments/assets/4ca7d140-c11d-40d1-ae9d-55c2728bb98a)
![Screenshot 2025-05-21 123044](https://github.com/user-attachments/assets/9ae17f8e-f4d9-492c-b658-c272db81b4f0)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
