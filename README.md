# vhostman for OSX

What is it?
===========

A little PHP script to quickly add, remove or list vhosts to your local apache configuration for development purposes on OSX.

Installation
============

Make a directory to contain all the generated vhost config files:
    
    sudo mkdir /etc/apache2/extra/vhosts
    
Add this line to your /etc/apache2/httpd.conf file:
    
    Include /private/etc/apache2/extra/vhosts/*.conf
    
Ensure it's executable:

    chmod u+x /path/to/vhostman
    
Link this into your /usr/local/bin like so:

    ln -s /path/to/vhostman /usr/local/bin/vhostman

Usage
=====

Show existing vhosts

    sudo vhostman list

Add a new vhost

    sudo vhostman add example.local ~/path/to/example

Remove an existing vhost

    sudo vhostman rm example.local