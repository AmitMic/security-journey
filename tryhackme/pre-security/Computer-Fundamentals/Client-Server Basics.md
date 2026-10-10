# Client-Server Basics

- **Main idea:** Understanding the Client-Server model and understanding this concepts on a surface level: DNS, Client, Server, Port, Protocol, Network.
  - **Client, Server:** A client is for example a website which can request things from the server, for example requesting to go to the webpage, and the server is the system which gives it to the client.
  - **Protocol:** A protocol defines how a client can communicate with a server.
  - **Port:** A port is used to identify a specific service running on a system. When a client wants to access a service on a server, it must connect using the correct port.
  - **DNS:** DNS which stands for Domain Name System is a protocol which helps translate human readable text to the IP addresses(basically the place the website is located at) of the websites the client wants to access.
  - **HTTP(S):** Is a stateless client-server protocol used for the world wide web. it basically means that each request is processed independently, without the server retaining information about previous requests. even though the protocol is stateless modern websites use something called a session identifier(cookie) which basically makes it so if u log into your account and than request to move to a page instead of needing to authenticate urself again it automatically keeps you logged in.

## Real Machine Practice
**In the room we have conducted an experiment that showed us what a client request and a server respond looks like behind the scenes, here is what I learned during the experiment:**
 - Get requests
 - Headers(specifically Scheme: tells us which protocol was used, https or http. host: Tells us the name of the host we request resources from. filename: shows which file we requested from the host. address: shows the ip address of where the website is hosted. and status: shows if the request was successful)
 - Navigation through the developer tools.

