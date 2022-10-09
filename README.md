# learning_nginx

<br>

# 1. Introduction to Nginx

-   Essentially a web server that uses a non-threaded, event driven architecture (async)
-   Can perform load balancing, http caching and used as a reverse proxy
-   Nginx has one master process and several worker processes.
-   Purpose of master process is to read and evaluate configuration and maintain worker processes.
-   Worker processes do actual processing of requests.

<br>

Configuration

-   The way nginx and its modules work is determined in the configuration file. By default, the configuration file is named nginx.conf and placed in the directory `/usr/local/nginx/conf`, `/etc/nginx`, or `/usr/local/etc/nginx`.

<br>

# 2. Basics of the Configuration File (nginx.conf)

-   The most important file as it acts as the default configuration entry point of the NGINX service.

<br>

-   `worker_processes`: Defines the number of worker processes that NGINX uses. As NGINX is single-threaded, this usually means the number of CPU cores used.
-   `worker_connections`: This directive defines the number of simultaneous connections each worker_process can serve
-   `access_log` and `error_log`: NGINX use these files to log all the access attempts and errors that will be encountered.
