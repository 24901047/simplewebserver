# EX01 Developing a Simple Webserver
## Date:

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
![WhatsApp Image 2024-12-14 at 7 56 50 AM](https://github.com/user-attachments/assets/a388fa70-0f05-4554-95a4-416c6643f9f6)
![Screenshot (10)](https://github.com/user-attachments/assets/d635f3dd-5027-4829-bdb4-a226a352f19a)


## RESULT:
The program for implementing simple webserver is executed successfully.
