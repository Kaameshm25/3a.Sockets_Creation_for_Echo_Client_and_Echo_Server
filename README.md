# Ex No :3a  CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME : KAAMESH M
## REGISTER NUMBER : 212223040080
## AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT 
```py
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    clientmessage=c.recv(1024).decode()
    c.send(clientmessage.encode())

```
### SERVER 
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```
## OUTPUT

### CLIENT OUTPUT

![CN 2c c](https://github.com/Kaameshm25/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870650/409ece4a-bb5b-4ce8-96fa-7a63465873c3)

### SERVER OUTPUT

![CN 3a S](https://github.com/Kaameshm25/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870650/2d738876-9ab2-4e1f-a843-66026428035f)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
