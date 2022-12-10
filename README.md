# Developing a Simple Webserver
# AIM:
To develop a simple webserver to display top five web application development languages

# DESIGN STEPS:
## Step 1: 
HTML content creation
## Step 2:
Design of webserver workflow
## Step 3:
Implementation using Python code
## Step 4:
Serving the HTML pages.
## Step 5:
Testing the webserver

# PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler
content='''
hello
'''
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(402)
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address=('',80)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```


# OUTPUT:


# RESULT:
