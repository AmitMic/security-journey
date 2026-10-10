# Client-Server Basics

- **Main idea:** The client-server model and the concepts that make it work: client, server, protocol, port, DNS, and HTTP/HTTPS.
  - **Client, Server:** A client is the device or software that requests something (e.g. my browser asking for a webpage). A server is the system that responds by providing it (e.g. the machine hosting the website).
  - **Protocol:** A protocol defines how a client and a server communicate.
  - **Port:** A port identifies a specific service running on a system. When a client wants to access a service on a server, it must connect using the correct port.
  - **DNS:** The Domain Name System is a protocol that translates human-readable domain names (like google.com) into the IP addresses (basically the location) of the websites the client wants to access.
  - **HTTP(S):** HTTP is a stateless client-server protocol used for the World Wide Web. Stateless means each request is processed independently, and the server doesn't retain information about previous requests. Even so, modern websites use a session identifier stored in a "cookie". If I log into my account and then move to another page, the cookie lets the site keep me logged in instead of making me authenticate again.
  - **HTTP vs. HTTPS:** HTTPS is a version of HTTP that encrypts the data being transferred, so people watching the network can't read it. HTTP is sent in plain text. (Observers can still usually see which server I connected to.)

## Real Machine Practice
In the room we ran an experiment that showed what a client request and a server response look like behind the scenes. Here is what I learned:
- **GET requests:** GET asks the server to send me a resource, like a page.
- **Headers:**
  - **Scheme:** the protocol used (HTTP or HTTPS)
  - **Host:** the name of the host we request resources from
  - **Filename:** the file requested from the host
  - **Address:** the IP address where the website is hosted
  - **Status:** whether the request succeeded (e.g. 200 = OK, 404 = Not Found)
- **Developer tools:** how to open the browser's developer tools and find these requests and headers.

- **Security angle:** HTTP sends data readable by anyone on the network, while HTTPS encrypts it. A stolen session cookie can let an attacker act as the logged-in user. Every open port is a service that could be attacked.
