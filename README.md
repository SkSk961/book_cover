# Ex.06 Book Front Cover Page Design
# Date:05/11/2024
# AIM:
To design a book front cover page using HTML and CSS.

# DESIGN STEPS:
## Step 1:
Create a Django Admin project.

## Step 2:
Create an app in the Django interface.

## Step 3:
Create a folder named 'static' in the app folder.

## Step 4:
Create a new HTML file in the static folder.

## Step 5:
Write the HTML code with relevant CSS properties.

## Step 6:
Choose the appropriate style and color scheme.

## Step 7:
Insert the images in their appropriate places.

## Step 8:
Publish the website in the LocalHost.

# PROGRAM:
~~~
from django.shortcuts import render
from http.server import BaseHTTPRequestHandler, HTTPServer
from importlib.resources import contents
from django.http import HttpResponse

content='''
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Book Design</title>
    <style>
        body {
            font-family: 'Verdana', sans-serif;
            background-color: #eaeaea;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .box {
            width: 450px;
            height: 650px;
            background-color: #ffffff;
            border: 1px solid #ddd;
            border-radius: 15px;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            position: relative;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }

        .image-container {
            height: 50%;
            overflow: hidden;
        }

        .image-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .content {
            padding: 20px;
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .title {
            font-size: 24px;
            font-weight: bold;
            color: #222;
            margin: 0;
        }

        .caption {
            font-size: 18px;
            font-style: italic;
            color: #555;
            margin: 15px 0;
        }

        .author {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .author img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            border: 2px solid #ddd;
            margin-right: 15px;
        }

        .author-name {
            font-size: 16px;
            font-weight: bold;
            color: #333;
        }

        .details {
            font-size: 14px;
            color: #888;
            text-align: right;
        }

        .strip {
            height: 5px;
            background: linear-gradient(to right, #ff7e5f, #feb47b);
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="image-container">
            <img src="https://img.freepik.com/free-photo/book-composition-with-open-book_23-2147690555.jpg" alt="Book Cover">
        </div>
        <div class="content">
            <div>
                <h1 class="title">The Art of Simplicity</h1>
                <p class="caption">"Simplicity is the ultimate sophistication."</p>
            </div>
            <div class="author">
                <img src="sharan.jpg" alt="Author">
                <div class="author-name">Sharan Kumar G (24001249)</div>
            </div>
            <div class="details">
                <div>Publisher: SimpleBooks</div>
                <div>2024</div>
            </div>
        </div>
        <div class="strip"></div>
    </div>
</body>
</html>

'''
from http.server import HTTPServer,BaseHTTPRequestHandler
class Myserver(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address = ('',8000)
httpd = HTTPServer(server_address,Myserver)
httpd.serve_forever()
~~~
# OUTPUT:
![Screenshot 2024-12-07 110104](https://github.com/user-attachments/assets/b2237a64-4eec-4237-901d-f9a9914bea03)
![Screenshot 2024-12-07 110848](https://github.com/user-attachments/assets/86032913-f767-445b-a697-d578b95cd357)


# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
