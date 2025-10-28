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


### client:

```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
msg=input("Client > ") 
s.send(msg.encode()) 
print("Server > ",s.recv(1024).decode())
```

### server:

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

### client:

<img width="610" height="203" alt="image" src="https://github.com/user-attachments/assets/40d92e61-7c28-4500-8f0d-e329aece3482" />

### server:

<img width="579" height="193" alt="image" src="https://github.com/user-attachments/assets/750278d6-6998-4728-8cb4-52370fa050eb" />

## OUPUT
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
