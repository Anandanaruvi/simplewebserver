# Developing a Simple Webserver

## AIM:

To develop a simple webserver to serve html pages.

## DESIGN STEPS:

### Step 1: 

HTML content creation

### Step 2: 

Design of webserver workflow


### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1><u>Languages used iun Web Development</u><h1>
<ul>
<li>HTML</li>
<li>CSS</li>
<li>JavaScript</li>
<li>Bootstrap</li>
</body>
</html>
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

![out1](https://user-images.githubusercontent.com/120443233/228129675-2d234c63-291b-4ec8-a5ad-119ce6bda1dc.png)


![out2](https://user-images.githubusercontent.com/120443233/228129780-180116a4-d5db-47bf-919a-f935743c3975.png)

## RESULT:

The program for implementing simple webserver is executed successfully.

