# 2a_Stop_and_Wait_Protocol
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
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())

## OUTPUT
![cn reveiver act 2a](https://github.com/user-attachments/assets/6f427efb-72d2-4547-a9e6-941d58c14267)
![cn activity 2a](https://github.com/user-attachments/assets/a2783f84-8e61-40c1-8ee3-28e7d5c12bdf)
![cmd prompt 1](https://github.com/user-attachments/assets/56de72ab-3db7-4f8c-8f68-71f93a7b046f)
![cmd prompt 1 2a](https://github.com/user-attachments/assets/1e935c60-4756-44b3-8bfd-993e67a8b783)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
