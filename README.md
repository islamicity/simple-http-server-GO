# simple-http-server-GO
Accompanying code for my youtube video

# Fungsi formHandler
This is a Go function that handles HTTP POST requests. It is defined as formHandler and takes two arguments, w and r. w is a http.ResponseWriter object that can be used to write the response to the client, and r is a *http.Request object that represents the incoming request.

The function starts by calling r.ParseForm() to parse the form data in the request body. If an error occurs during parsing, it is returned to the caller with a message indicating the error.

Next, the function writes the string "POST request successful" to the http.ResponseWriter object. It then retrieves the values of the "name" and "address" form fields by calling r.FormValue("name") and r.FormValue("address"), respectively. Finally, the values of name and address are written to the http.ResponseWriter object using fmt.Fprintf.


Fungsi helloHandler
This is a Go function that handles HTTP GET requests for the "/hello" endpoint. It is defined as helloHandler and takes two arguments, w and r. w is a http.ResponseWriter object that can be used to write the response to the client, and r is a *http.Request object that represents the incoming request.

The function starts by checking if the request URL path is "/hello". If not, it returns a 404 error to the client using the http.Error function.

Next, the function checks if the request method is "GET". If it's not, it returns a "method is not supported" error to the client.

Finally, if the URL path and method are both correct, the function writes the string "hello!" to the http.ResponseWriter object using fmt.Fprintf.



Regenerate response
