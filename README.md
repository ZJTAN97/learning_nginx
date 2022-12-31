# learning_nginx

<br>

# Introduction to Nginx

-   Essentially a web server that uses a non-threaded, event driven architecture (async) and serves web content
-   Can perform load balancing, http caching and used as a reverse proxy
-   Nginx has one master process and several worker processes.
-   Purpose of master process is to read and evaluate configuration and maintain worker processes.
-   Worker processes do actual processing of requests.

<br>

Configuration

-   The way nginx and its modules work is determined in the configuration file. By default, the configuration file is named nginx.conf and placed in the directory `/usr/local/nginx/conf`, `/etc/nginx`, or `/usr/local/etc/nginx`.

<br>
<br>

# Layer 4 vs Layer 7 proxying

-   Layer 1 --> Physical Layer
-   Layer 2 --> Data Link Layer
-   Layer 3 --> Network Layer
-   Layer 4 --> Transport Layer
-   Layer 5 --> Session Layer
-   Layer 6 --> Presentation Layer
-   Layer 7 --> Application Layer

<br>

-   In layer 4, we see TCP/IP stack only, nothing about the app, we have access to

    -   Source IP, Source Port
    -   Destination IP, Destination Port
    -   Simple packet inspection (SYN/TLS hello)

-   In Layer 7, we see the application, HTTP/gRPC etc

    -   More access to context
    -   Know where the client is going, which page they are visiting
    -   Require decryption

-   NGINX can operate in layer 7 (http) or layer 4 (tcp)

<br>
<br>

# Basics of the Configuration File (nginx.conf)

-   The most important file as it acts as the default configuration entry point of the NGINX service.

<br>

-   `worker_processes`: Defines the number of worker processes that NGINX uses. As NGINX is single-threaded, this usually means the number of CPU cores used.
-   `worker_connections`: This directive defines the number of simultaneous connections each worker_process can serve
-   `access_log` and `error_log`: NGINX use these files to log all the access attempts and errors that will be encountered.
