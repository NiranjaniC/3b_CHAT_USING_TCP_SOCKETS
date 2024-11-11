# 3b.CREATION FOR CHAT USING TCP SOCKETS
## DATE:24/09/2024
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## server.py
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```

## OUTPUT
## client
![Screenshot 2024-10-22 094032](https://github.com/user-attachments/assets/81f77d72-7191-45e0-8a60-873e188c6a36)
## server
![Screenshot 2024-10-22 093956](https://github.com/user-attachments/assets/af87d66a-eca0-41d1-8241-9d05cad96ef8)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
