# 2a_Stop_and_Wait_Protocol
### Name : Aadithya R
### Reg.No : 212223240001
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
### CLIENT
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
### SERVER
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>

## OUTPUT
### CLIENT
![Screenshot 2024-09-03 084238](https://github.com/user-attachments/assets/53924fd2-98be-47af-bdbb-c293312d1947)


### SERVER
![Screenshot 2024-09-03 084250](https://github.com/user-attachments/assets/a074fd69-d02c-4763-ab7a-d0261f015fe6)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
