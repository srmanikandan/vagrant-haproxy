# vagrant-haproxy
Vagrant-haproxy.
Demo of HAProxy high availability using Vagrant.

This project sets up the following VMs on a private network in VirtualBox:

haproxy (172.28.128.10)
web1 (172.28.128.11)
web2 (172.28.128.12)


Prerequisites
Install Vagrant
Install Virtualbox

Getting started
From the root directory, run vagrant up (Vagrant file consist all the needed configuration.)
View the various pages:
source web sites: e.g., http://172.28.128.10
web1 page e.g., http://172.28.128.11
web2 page e.g., http://172.28.128.12

Bring any one of the web server down and still the loadbalance servers the request to the other webserver.

