![clientoutput](https://github.com/hasinimarella/webserver/assets/147473417/f3c498b9-54fe-4f1f-8d06-73987547273e)# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```py
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
<h2>1.Django</h2>
<h2>2. MEAN Stack</h2>
<h2>3. React </h2>
<h2>4.MERN Stack</h2>
<h2>5.ASP.Net</h2>
</body>
</html>
'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',80)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```

## OUTPUT:
### Server output
![serveroutput](https://github.com/hasinimarella/webserver/assets/147473417/fc655e23-a8af-4afd-9ca7-c6264a3a5f49)
### Client output
![clientoutput](https://github.com/hasinimarella/webserver/assets/147473417/0a8cfb3c-d4e4-4358-ae32-116eebff68d1)

## RESULT:
The program is executed succesfully
