# Echoserver
Echo server and client using python socket

## Name: JeshwanthKumarpayyavula
## Register.No:212223240114

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
### Client.py
```
import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Jeshwanth Kumar , 212223240114,18-03-2025")
    data = s.recv(1024)


print(f"Received {data!r}")
```
### Server.py
```
import socket


HOST = "127.0.0.1"  
PORT = 65432  


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```


## OUTPUT:
![image](https://github.com/user-attachments/assets/073778dd-183c-4790-80dd-015a5df5164d)


## RESULT:
The program is executed successfully
