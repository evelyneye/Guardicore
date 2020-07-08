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

├── Assignment_v2

│   ├── Files

│   │   ├── cli.ini

│   │   ├── haproxy.conf

│   │   ├── nginx.conf

│   │   └── test.html

│   ├── certbot.yml

│   ├── handlers

│   │   └── main.yml

│   ├── haproxy.yml

│   ├── inventory

│   ├── iptables-haproxy.yml

│   ├── iptables-nginx.yml

│   ├── main.yml

│   ├── nginx.yml

│   ├── run-certbot.j2

│   ├── setup_certbot_script.yml

│   └── ssh.yml

└── README.md
