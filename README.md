# Guardicore

Ansible assignment:

In this assignment you will need to configure secure and redundant website by using ansible.


* Nginx and HA Proxy will be installed by downloading and compiling the sources
* HA proxy needs to balance the traffic between two website (Machine B and machine C)
* web server on machine B and C should listen on port 8080
* When someone is opening https://<machine_A_IP>/test.html he will get valid SSL website with “hello world page”, the ha_proxy should serve the ssl certificate (use let’s encrypt), any other page should redirect the client to https://www.google.com
* All the machines should be secure with IPtables (you need to block everything except the service ports and ssh ports)
* SSH login to machine C and B will be allowed only with keys
* Make sure everything works even after a reboot.

-----------------------
Project Structure 
-----------------------

├── Assignment_v2

│   ├── Files   //Including configuration files, index files

│   │   ├── cli.ini   //Certbot config

│   │   ├── haproxy.conf    //HAProxy config

│   │   ├── nginx.conf    //nginx config

│   │   └── test.html     //index page

│   ├── certbot.yml   //Certbot Installation and Configuration

│   ├── handlers    

│   │   └── main.yml    //Restart services tasks

│   ├── haproxy.yml   //Haproxy Installation and Configuration

│   ├── inventory   //Hosts

│   ├── iptables-haproxy.yml    //iptables configurations - haproxy

│   ├── iptables-nginx.yml    //iptables configurations - nginx

│   ├── main.yml    //Master playbook

│   ├── nginx.yml   //nginx Installation and Configuration

│   ├── run-certbot.j2    //Generate certificate

│   ├── setup_certbot_script.yml    //Setup certbot script and link cronjob to renew cert

│   └── ssh.yml   //Disable password authentication 

└── README.md
