
# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## ROLL: 21222324014
## NAME: NARESH.R
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
## client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## server:
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
## OUPUT
## CLINT
![image](https://github.com/feryjfgkuyfgewjfgew/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/150319377/6a237483-ec72-42cd-9463-53606076d4d6)

## SERVER
![Screenshot 2024-05-17 185718](https://github.com/feryjfgkuyfgewjfgew/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/150319377/97c20da5-2d54-452a-a369-d8d57a81b7f7)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
