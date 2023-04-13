# ansible-jenkins-aws
STEP1: (AWC-CONSOLE)
    * Created an AL2023 EC2 instance - Jenkins_server
      Security Group:
          - HTTP -80 PORT 
          - SSH - 20 PORT 
          - TCP - 8080 PORT for Jenkins
    * Created an AL2023 EC2 instance - Application_server-Host where application is hosted
    
STEP2: ssh to Jenkins_server(ec2) using putty
    * Installed Jenkins and Ansible
    * In .ssh directory create public and private RSA key
    * Copied the RSA public key to .ssh directory of Application_server. Thereby connection between the master and slave host is established
    
STEP3: http://<Jenkin_server public_ip>:8080---> Jenkins in Jenkins_server
    * Installed Ansible plugin 
    * Create a Job with pipeline and created declarative pipeline script, to connect to GitHub and the Application_server using pipeline sysntax
    
    
Note:
Ansible pipeline script:
  - initiated apache.yml and inventory file 
  - disable ssh_host_connect
  - copied the key.pem file to private key
