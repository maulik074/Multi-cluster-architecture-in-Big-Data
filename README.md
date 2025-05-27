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

3. All systems were connected to the DHCP server and validated using ping commands to ensure successful network communication.

4. **Key Generation and SSH Config** :- Created a RSA based SSH login-key for master using: ssh-keygen-t rsa-P ””
  
   A .ssh/config file was created to simplify host access using this command: gedit ˜/.ssh/config

5. Passwordless SSH access was configured using:
  
    ssh-copy-id master
  
    ssh-copy-id worker1
  
    ssh-copy-id worker2
  
    ssh-copy-id worker3
  
    ssh-copy-id worker4
  
    Verifying correct working of ssh using: 
  
    ssh worker1

6. **Apache Spark Cluster Setup :- **  We have created spark-env.sh from spark-env.sh.template and workers from workers.template.

7. We had started the cluster using this command : start-worker.sh spark://master:7077

   



