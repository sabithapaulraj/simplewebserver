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
content="""
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1>TOP FIVE WEB APPLICATION DEVELOPMENT</h1>
<h2> hello </h2>
</body>
</html>
"""
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header('content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address=('',8080)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```


# OUTPUT:

##Server Side Output
![Screenshot (40)](https://user-images.githubusercontent.com/118343379/206829581-1a221c62-f0a3-4327-8dd4-bf4842c5d48c.png)



##Client Side Output
![Screenshot (34)](https://user-images.githubusercontent.com/118343379/206829707-914d35b4-d20b-4e13-af5a-48f373fb5f1b.png)




# RESULT:
Thus the webserver is developed to display about top five programming languages.
