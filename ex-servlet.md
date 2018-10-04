# Servlet 4 and HTTP/2 Support Exercise

## Introduction

The main feature of the Servlet 4.0 API is to provide HTTP/2 support. In this exercise, we will see what it takes to HTTP/2 enable the simple Web application that we have developed in the previous exercise.

Check the URL of the application, it connects in clear (i.e. using http) to the port 8080. Now adjust the url to use *https* instead of *http* and to connect to port *8181* instead of port *8080* and connect to that updated URL.

Chrome will complain by saying that "*Your connection is not private*"; click on *ADVANCED* and then on *Procceed to locahost (unsafe)*.

![Your connection is not private](https://github.com/dheffelfinger/j1-hol/blob/master/pic/picservlet-1.jpg?raw=true)

:warning: Chrome complains because GlassFish is using, by default, a self-signed certificate. So while the connection between the browser and GlassFish is encrypted (TLS), it can't be trusted. In your application, you should use a certifacate that you can get from a trusted [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority). For the sake of this exercise, we can ignore this warning.

Login as *ed/ED*, you should see the main page of the application and a small blue lightning at the top right corner. This is Chrome HTTP/2 indicator; *blue* means that the connection is server over HTTP/2. Clicking on it will show details on the HTTP/2 connection (streams, frames, etc.). This is really all it takes to HTTP/2 enable an exisiting Servlet application, just deploy on a Servlet 4 container! 

![Chorome HTTP/2 indicator"](https://github.com/dheffelfinger/j1-hol/blob/master/pic/picservlet-2.jpg?raw=true)

### Back to the [Exercices list](https://github.com/dheffelfinger/j1-hol#java-ee-8-hands-on-lab).

