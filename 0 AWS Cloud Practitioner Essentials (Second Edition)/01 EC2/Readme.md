# EC2

## Acronym
* SDK - Software Development Kit
* CLI - Command Line Interface
* S3 - Scalable Storage in the Cloud
* EIP - Elastic IP Address
* VPC - Virtual Private Cloud
* EC2 - Elastic Compute Cloud
* SW - Software
* HW - Hardware
* AMI - Amazon Machine Image
* NIC - Network Interface Card

## AWS Console
### Region
* Choose your region (where the EC2 instance will be hosted)

[<img src="https://i.imgur.com/zG4qXmQ.png">](https://i.imgur.com/zG4qXmQ.png)

### Services
* Services\EC2

[<img src="https://i.imgur.com/JWyMHoT.png">](https://i.imgur.com/JWyMHoT.png)
* Launch instance

[<img src="https://i.imgur.com/oQ6juLX.png">](https://i.imgur.com/oQ6juLX.png)
* Amazon Linux AMI 2018.03 (HVM), SSD Volume Type

[<img src="https://i.imgur.com/DRZShnR.png">](https://i.imgur.com/DRZShnR.png)
#### Instance Type
1) Chosse your Type, vCPUs, Memory (GiB), and sot on

[<img src="https://i.imgur.com/DpuUW3z.png">](https://i.imgur.com/DpuUW3z.png)

2) Choose : 
    * Nbr instance, 
    * Network
    * Subnet
    * and so on

[<img src="https://i.imgur.com/BoIblRp.png">](https://i.imgur.com/BoIblRp.png)

3) Add Storage

[<img src="https://i.imgur.com/g8AGUCd.png">](https://i.imgur.com/g8AGUCd.png)

4) Add Tags
* A tag consists of a case-sensitive key-value pari
      * E.g. tag with key = Name & Value = Webserver
* A copy of a tag can be applied to volumes, instances or both

[<img src="https://i.imgur.com/FNUjTTC.png">](https://i.imgur.com/FNUjTTC.png)
[<img src="https://i.imgur.com/Oj8uUHR.png">](https://i.imgur.com/Oj8uUHR.png)

5) Configure Security Group (firewall)
* Create or select ... security group
      * Security group name
      * Description
* Type
   * Custom TCP Rule
   * Custom UDP Rule
   * Custom ICMP Rule - IPv4
   * Custom ICMP Rule - IPv6
   * Custom Protocol
   * All TCP
   * All UDP
   * All ICMP - IPv4
   * All ICMP - IPv6
   * All traffic
   * SSH
   * SMTP
   * DNS (UDP)
   * DNS (TCP)
   * HTTP
   * POP3
   * IMAP
   * LDAP
   * HTTPS
   * SMB
   * SMTPS
   * IMAPS
   * POP3S
   * MS SQL
   * NFS
   * MYSQL/Aurora
   * RDP
   * Redshift
   * PostgreSQL
   * Oracle-RDS
   * WinRM-HTTP
   * WinRM-HTTPS
   * Elastic Graphics
   
[<img src="https://i.imgur.com/st67M4J.png">](https://i.imgur.com/st67M4J.png)

6) Review Instance Lauch

[<img src="https://i.imgur.com/bt9Q4LK.png">](https://i.imgur.com/bt9Q4LK.png)

7) An existing key pair or create a new key pari
* Create a new key pair
      * key pair name
      * Download key pair (*.pem)
      
[<img src="https://i.imgur.com/jhmHbdV.png">](https://i.imgur.com/jhmHbdV.png)

8) Lanch Status

[<img src="https://i.imgur.com/yxiAwOa.png">](https://i.imgur.com/yxiAwOa.png)
[<img src="https://i.imgur.com/jkQMAtt.png">](https://i.imgur.com/jkQMAtt.png)

## SSH
* Default user : ec2-user
### puttygen
* Convert \*.pem -> \*.ppk

        * Open puttygen.exe\load *.pem

[<img src="https://i.imgur.com/aHW1lpQ.png">](https://i.imgur.com/aHW1lpQ.png)

[<img src="https://i.imgur.com/7k7Dy4d.png">](https://i.imgur.com/7k7Dy4d.png)

[<img src="https://i.imgur.com/BFkmXre.png">](https://i.imgur.com/BFkmXre.png)

### putty
* Connection\SSH\Auth\Browse...\*.ppk
* host name\UserName@PublicIP

[<img src="https://i.imgur.com/hkoHIYA.png">](https://i.imgur.com/hkoHIYA.png)

[<img src="https://i.imgur.com/ycxF4i9.png">](https://i.imgur.com/ycxF4i9.png)

````Bash
# Fedora
cat /etc/*release
````
[<img src="https://i.imgur.com/Lc0yfoC.png">](https://i.imgur.com/Lc0yfoC.png)

````Bash
#old version
aws --version
````
[<img src="https://i.imgur.com/zmGzx7L.png">](https://i.imgur.com/zmGzx7L.png)

## AMI

### [Windows](https://i.imgur.com/wgPLW74.png)
#### Free
1) Windows Server 2019 Base
2) Windows Server 2019 Base with Containers
3) Windows Server 1909 core Base
4) Windows Server 2016 Base
5) Windows Server 2016 Base with Containers
6) Windows Server 2016 with SQL Server 2019 Standard

#### No Free
1) 

### Linux
#### Free
##### AMI
1) Amazon Linux AMI 2018.03.0 (fedora)
   * default-user: ec2-user
   
2) Ubuntu Server 18.04 LTS
   * default-user: ubuntu
   
##### Marketplace
1) CentOS 7
   * default-user: centos

#### htop
[<img src="https://i.imgur.com/H53Pa62.png">](https://i.imgur.com/H53Pa62.png)

## Windows Server 2019 Base
### Default
* CPU: Xeon E5-2673 v3 @ 2.4GHz
* RAM: 1Go

[<img src="https://i.imgur.com/jNFAXfw.png">](https://i.imgur.com/jNFAXfw.png)

* Hostname

[<img src="https://i.imgur.com/n1qemp0.png">](https://i.imgur.com/n1qemp0.png)

### Winver
* WS2019-Datacenter

[<img src="https://i.imgur.com/wxm7kUr.png">](https://i.imgur.com/wxm7kUr.png)

### NIC
* IPv4: 172.31.18.137/20 & gw.1
* DNS: 172.31.0.2
* DHCP: 173.31.16.1

[<img src="https://i.imgur.com/XnFIrR5.png">](https://i.imgur.com/XnFIrR5.png)
[<img src="https://i.imgur.com/IBndX6v.png">](https://i.imgur.com/IBndX6v.png)

## Startup cmd
