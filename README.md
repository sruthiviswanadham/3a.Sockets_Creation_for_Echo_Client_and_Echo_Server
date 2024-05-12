## EXP NO 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

## NAME: VISWANADHAM VENKATA SAI SRUTHI
## REG NO: 212223100061

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
## Client:

```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
clientMessage=c.recv(1024).decode()
c.send((clientMessage.encode()))
```
## Server:

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
msg=input("client>")
s.send(msg.encode())
print("server>",s.recv(1024).decode())
```
## OUtPUT
## Client:

![image](https://github.com/sruthiviswanadham/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151760421/145df2c0-c3d5-4c9c-a11f-81be4fc9750d)

## Server:

![image](https://github.com/sruthiviswanadham/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151760421/d2de8e50-4c6b-455d-8ec2-df730c6a5d48)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
