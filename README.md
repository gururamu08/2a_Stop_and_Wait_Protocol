# Ex-2a Stop_and_Wait_Protocol
## Register Number: 212222230042
## Name: GURUMOORTHI R
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
### Client:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
   print(ack)
   continue
 else:
   c.close()
   break
```
### Server:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
## OUTPUT
### Client:

![exp 1a a](https://github.com/gururamu08/2a_Stop_and_Wait_Protocol/assets/118707009/7ed86ca2-2084-4484-9621-a97691644e50)


### Server:

![exp 1a b](https://github.com/gururamu08/2a_Stop_and_Wait_Protocol/assets/118707009/fc48d236-8ead-4224-8eda-2f0a7b9ddb7a)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
