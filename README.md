a# EX01 Developing a Simple Webserver
## Date:12/4/25
##Name: Abhishek kannan M
## Reg no: 21222404007

## AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
<th>Processor</th>
                    <th>i5</th>
                </tr>
                <tr>
                    <th'''
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<doctype html>
    <html>
        <head>
            <b><center>LAPTOP CONFIGURATION</center></b>
        </head>
        <BODY>
            <center>
            <table border= "2" bgcolor="grey" cellpadding="10" cellspacing="5" allign="center">
                <tr>
                    <th>System configuration</th>
                    <th> Description</th>
                </tr>
                <tr>>Primary Memory</th>
                    <th>Ram 16 GB</th>
               </tr>
                <tr>
                    <th>Secondary Memory</th>
                    <th>512 GB</th>
                </tr>
                <tr>
                    <th>0.S</th>
                    <th>Windows 11</th>
                </tr>
                <tr>
                    <th>Graphic</th>
                    <th>nvidia</th>
                </tr>
                </table>
            </center>
            
        </BODY>
'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
'''

                

## OUTPUT:
![Screenshot 2025-04-12 050954](https://github.com/user-attachments/assets/07557fd0-0bf1-4739-8f70-b5783a4c488b)
![Screenshot 2025-04-12 051031](https://github.com/user-attachments/assets/f54452ae-4a24-4484-98c1-fc0c6bf05440)


## RESULT:
The program for implementing simple webserver is executed successfully.
