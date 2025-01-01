# Use a base image of Debian as specified in the exploit details
FROM debian:bullseye

# Install necessary tools, libraries, and APR
RUN apt-get update && \
    apt-get install -y wget build-essential libpcre3-dev libssl-dev libapr1-dev libaprutil1-dev

# Download the specified Apache version
RUN wget https://archive.apache.org/dist/httpd/httpd-2.4.50.tar.gz && \
    tar -xzf httpd-2.4.50.tar.gz

# Install Apache with necessary modules for CGI
RUN cd httpd-2.4.50 && \
    ./configure --enable-cgi --enable-ssl --enable-so && \
    make && \
    make install

# Configure Apache to start with the system
COPY my-httpd.conf /usr/local/apache2/conf/httpd.conf

# Expose the Apache port
EXPOSE 80

# Start Apache in the foreground
CMD ["/usr/local/apache2/bin/httpd", "-D", "FOREGROUND"]
