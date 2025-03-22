# EX01 Developing a Simple Webserver
## Date:22.03.2025
## ROLL NO: 212224230310


## AIM:
To develop a simple webserver to serve html pages and display the tabular column of multiple Companies and its Revenue

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
<head>
<title>Top Software Industries</title>
</head>
<body>
<table border="2" cellspacing="10" cellpadding="6">
<caption>Top 5 Revenue Generating Software Companies</caption>
<tr>
<th>S.No</th>
<th>Companies</th>
<th>Revenue</th>
</tr>
<tr>
<th>1</th>
<th>Microsoft</th>
<th>65 billion</th>
</tr>
<tr>
<th>2</th>
<th>Oracle</th>
<th>29.6 billion</th>
</tr>
<tr>
<th>3</th>
<th>IBM</th>
<th>29.1 billion</th>
</tr>
<tr>
<th>4</th>
<th>SAP</th>
<th>6.4 billion</th>
</tr>
<tr>
<th>5</th>
<th>Symantec</th>
<th>5.6 billi
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```


## OUTPUT:
![Screenshot 2025-03-18 052328](https://github.com/user-attachments/assets/edd15578-bb81-49d0-b607-ac0d50e8c5a1)
![Screenshot 2025-03-18 052342](https://github.com/user-attachments/assets/7cf7f456-fa6c-4969-8c53-6821a4bebb0e)



## RESULT:
The program for implementing simple webserver is executed successfully.

