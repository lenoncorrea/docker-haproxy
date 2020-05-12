# HAProxy and WebServer
Examples of configuration for your web servers 

# Commands
Run a simple command in folder docker: 
"docker-compose up -d"

**Change the necessary settings for your application in the "./haproxy/haproxy.cfg" file**

## Diagram operation
```mermaid
graph LR
A[HAProxy]
A -- Resquest 1, 3, 5... --> B(Apache_Web_1)
A -- Resquest 2, 4, 6... --> C(Apache_Web_2)
B --> D{Database}
C --> D

## Consult Official Documentations in Docker Hub
**Apache**: https://hub.docker.com/_/httpd
**HAProxy**:https://hub.docker.com/_/haproxy