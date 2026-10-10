# Client-Server Basics

## Main idea
The client-server model and the concepts that make it work: client, server, protocol, port, DNS, and HTTP/HTTPS.

## Key concepts
- **Client and server:** a client is the device or software that requests something (e.g. my browser asking for a webpage). A server is the system that responds by providing it (e.g. the machine hosting the website).
- **Protocol:** a protocol defines how a client and a server communicate: the agreed rules for the format and order of messages. Examples: HTTP (web pages), DNS (looking up names), SSH (remote login).
- **Port:** a port identifies a specific service running on a system. If the IP address is the building, the port is the door to one particular service. A client must connect to the correct port to reach a service. Common examples: 80 (HTTP), 443 (HTTPS), 22 (SSH), 53 (DNS).
- **DNS:** the Domain Name System is a protocol that translates human-readable domain names (like google.com) into the IP addresses (basically the location) of the websites the client wants to access.
- **HTTP(S):** HTTP is a stateless client-server protocol used for the World Wide Web. Stateless means each request is processed independently, and the server doesn't retain information about previous requests. Even so, modern websites use a session identifier stored in a "cookie". If I log into my account and then move to another page, the cookie lets the site keep me logged in instead of making me authenticate again.
- **HTTP vs. HTTPS:** HTTPS is a version of HTTP that encrypts the data being transferred, so people watching the network can't read it. HTTP is sent in plain text. (Observers can still usually see which server I connected to.)
- **HTTP headers:** extra information sent along with a request or response, as `Name: value` pairs. Examples: `Host` (which site I'm asking for), `User-Agent` (which browser I'm using), `Cookie` (my session identifier, sent with each request), `Set-Cookie` (the server giving me a cookie), `Content-Type` (what kind of data came back).

## Hands-on
In the room we ran an experiment that showed what a client request and a server response look like behind the scenes.
- **GET request:** asks the server to send me a resource, like a page.
- **What the browser's Network tab shows for a request:**
  - **Scheme:** the protocol used (HTTP or HTTPS). Part of the URL.
  - **Host:** the name of the host we request resources from. Part of the URL (also sent as the `Host` header).
  - **Filename:** the file requested from the host. Part of the URL.
  - **Address:** the IP address where the website is hosted.
  - **Status:** whether the request succeeded (e.g. 200 = OK, 404 = Not Found). This belongs to the server's response.
- **Developer tools:** how to open the browser's developer tools and find these requests. The real headers are in the Headers tab of each request.

## Security angle
- HTTP sends data readable by anyone on the network, while HTTPS encrypts it.
- A stolen session cookie can let an attacker act as the logged-in user.
- Every open port is a service that could be attacked.
