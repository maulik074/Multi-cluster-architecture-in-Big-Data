# Multi-cluster-architecture-in-Big-Data

In this project, we have deployed a multi-node Apache Spark cluster to solve real-world big data processing tasks. The cluster consists of one master and four worker nodes, configured with static IP assignments via a custom DHCP server and SSH-based password-less authentication. This project highlights the practical challenges and solutions in deploying distributed systems for big data analytics.

## Steps and Working

1. A custom DHCP server was implemented to manage IP addresses for all cluster nodes. Static IPs were assigned based on MAC addresses to ensure consistent identity across restarts.

2. Each system’s /etc/hosts file was edited to map static IPs to hostnames:
192.168.43.101 master
192.168.43.102 worker1
192.168.43.103 worker2
192.168.43.104 worker3
192.168.43.105 worker4



