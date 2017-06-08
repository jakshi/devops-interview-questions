# DevOps Engineer assignment

This document contains description and requirements for assignment for DevOps Engineer position.

## Requirements

## Goal

1. Verify candidate's ability to work with Docker
2. Verify candidate's ability to create running environment with different services
3. Verify candidate's ability to setup services with security in mind

### Docker - PHP - NodeJS

* For PHP: Wordpress, for NodeJS: Ghost
* Create 2 different docker environments using docker-compose, each service in the environment should run in a separate container, make sure using latest v2 syntax

    * Database (MySQL, MariaDB)
    * PHP-FPM
    * NodeJS
    * Nginx
    * Data container for files

* Make sure all data will be persistent using volume mounts
* Make sure services will start in the right order (i.e. wait for mysql initialization)
* Add a custom configuration to Nginx

    * Enable HTTPS and redirect HTTP to HTTPS
    * Create a self-signed certificate or use LetsEncrypt, also document the commands you are using to create the certificate
    * Use TLS only
    * Use strong ciphers only
    * Generate a DH key and enable dhparam, also document the commands you are using to create a dh key
    * Enable	HSTS
    * Enable OCSP Stapling
    * Enable Nginx Microcaching and make sure Cache is not enabled in Admin Area and for logged in users
    * Add any other configuration you may think is important (headers, deny access to important files and folders, ...)

* Add a custom php-fpm config

    * For process management: choose either static, on demand, dynamic, also explain your decision
    * Listen directive: choose either Socket or TCP, also explain your decision
    * Add any other configuration you may think is important (number of workers, timeout, …)

* Commit both projects to Github and write your explanations and documentations into the readme
* Both environments need to work after we clone it and run docker-compose up

### Cache - Redis - Memcached

* Create two Service Unit files to start a Redis and Memcached docker container on a CoreOS Cluster using fleetctl

    * Make sure when starting the service it will run only on one host in the cluster
    * Make sure after a restart, cached data is persistent (if possible)

* Create a Timer Unit File to execute a self written script by yourself (bash, python, ..) every 5 minutes to load some dummy data into Redis (can be simple key/value i.e. hello/world)

* Commit all files to Github, write some documentation into the readme how to load and start the service units and how to execute the timer unit

