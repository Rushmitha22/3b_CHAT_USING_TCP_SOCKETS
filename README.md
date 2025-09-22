# EXPERIMENT 3B: CREATION FOR CHAT USING TCP SOCKETS:
## NAME : RUSHMITHA R
## REGISTRATION NUMBER : 212224040281

## AIM:
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
### Server :
```
# server
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

### Client :

```
#client
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUTPUT :

### Server :

<img width="361" height="292" alt="3b server" src="https://github.com/user-attachments/assets/ef11ebdb-29c9-4837-865d-10363ed2df85" />

### Client :

<img width="537" height="491" alt="3b client" src="https://github.com/user-attachments/assets/f3cf776b-8a9f-4faa-872b-6ce85aef5115" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
