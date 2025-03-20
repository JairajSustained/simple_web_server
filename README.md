# Simple Web Server

This is a basic web server built with Go that demonstrates handling HTTP requests, serving static files, and processing form submissions.

## Features

- Static file serving
- Form handling with POST requests
- Simple GET endpoint

## Installation

Make sure you have Go installed on your system. Then clone this repository:

```bash
git clone https://github.com/JairajSustained/simple_web_server.git
cd simple_web_server
```

## Project Structure

```
simple_web_server/
├── main.go        # Main server code
└── static/        # Static files directory
```

## Usage

1. Start the server:

```bash
go run main.go
```

2. The server will start on port 8080:
```
Starting server at port 8080
```

3. Access the following endpoints:
   - `http://localhost:8080/` - Serves static files from the `./static` directory
   - `http://localhost:8080/hello` - Returns a simple "hello" message (GET only)
   - `http://localhost:8080/form` - Processes form submissions (POST)

## Form Submission

The form handler expects two fields:
- `name`: User's name
- `address`: User's address

Example HTML form for testing:

```html
<form action="/form" method="POST">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name"><br>
    <label for="address">Address:</label>
    <input type="text" id="address" name="address"><br>
    <input type="submit" value="Submit">
</form>
```

## API Endpoints

### GET /hello
Returns a simple "hello" message.

### POST /form
Processes form data and returns the submitted name and address.


