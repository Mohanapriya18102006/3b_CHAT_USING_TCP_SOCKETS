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

CLIENT:
```
CLIENT: 
 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```

SERVER:
```
SERVER: 
 
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
## OUPUT

CLIENT:
![Screenshot 2025-04-16 224051](https://github.com/user-attachments/assets/02d933c6-857d-4272-af9b-16abf73f7402)

SERVER:
![Screenshot 2025-04-16 224153](https://github.com/user-attachments/assets/39f2b5b3-1796-40f9-982e-e5879e799555)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
