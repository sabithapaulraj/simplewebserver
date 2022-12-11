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
![Screenshot (43)](https://user-images.githubusercontent.com/118343379/206890480-a5e3bc74-e541-46bf-bbf6-58f894be542d.png)




##Client Side Output
![Screenshot (45)](https://user-images.githubusercontent.com/118343379/206890491-db7bf69c-aabd-4c26-9007-e9f85d665e8d.png)





# RESULT:
Thus the webserver is developed to display about top five programming languages.
