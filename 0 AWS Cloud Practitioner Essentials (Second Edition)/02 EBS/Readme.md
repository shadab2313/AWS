# EBS

## Doc
[Amazon EBS Volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html?icmpid=docs_ec2_console)
[AWS Key Management Service Documentation](https://docs.aws.amazon.com/kms/index.html#lang/en_us)

## Teminology
* IOPS
  * IOPS 100/3000
    * Baseline of 3 IOPS per GiB with a min of 100 IOPS, bustable to 3000 IOPS

## Acronym
* EBS - Elastic Block Store
* SSD - Solid-State drive
* HDD - Hard Drive Disk
* gp - General purpose
* IOPS - I/O operation per second that the volume can support
* AZ - Availability Zone

## Overview - EBS Volumes
* Choose between HDD & SSD types
* Persisten & customizable block storage for EC2 instances
* Replicated in the same Availability zone
* Backup using Snapshots
* Easy & transparent Encryption
* Elastic volumes

## Drive Types
1) General Porpose SSD (gp2)
 * IOPS (Default) : 100/3000

2) Provisioned IOPS SSD (io1)

3) Cold HDD (sc1)

4) Throughput Optimized HDD (st1)

5) Magnetic (std)
 * Cheaper
 * Logs
 
 [<img src="https://i.imgur.com/0qatksI.png">](https://i.imgur.com/0qatksI.png)
  
## Snapshots
  * Volumes
  * Re-create volume from snapshot at any time
  * Share a snapshot
  * Copy a snapshots to a different AWS Region for even greater disater recovery protection
    *E.g
      * Encrypt & share form Virgina to Tokyo your snapshots

## Encryption
* No additonal cost

## Elasticity
* EBS volumes have the ability to increase capacity
  * E.g
    * 50GB -> 16 TB without needing to stop the instances
* EBS volume can change to different types

## Demo
### One Disk (OS)
* AWS Console\EC2\

[<img src="https://i.imgur.com/BIsKSjp.png">](https://i.imgur.com/BIsKSjp.png)

* Elastic Block Store\Volumes

[<img src="https://i.imgur.com/qlaHJql.png">](https://i.imgur.com/qlaHJql.png)

### New Volume

* Create Volume
 * Volume type
 * Size (GiB)
 * IOPS
 * Availability Zone (AZ EBS = EC2) 
 * [Snapshot](https://i.imgur.com/VKM9WUr.png)
 * Encryption
 * Add tag (Optional)
 
[<img src="https://i.imgur.com/cUzcnRJ.png">](https://i.imgur.com/cUzcnRJ.png)

* Name (object)

[<img src="https://i.imgur.com/teRWXNr.png">](https://i.imgur.com/teRWXNr.png)

### Attach Volume
* Action\Attach Volume

[<img src="https://i.imgur.com/XhuosWi.png">](https://i.imgur.com/XhuosWi.png)

[<img src="https://i.imgur.com/5iBA906.png">](https://i.imgur.com/5iBA906.png)

### New disk (not FileSystem)
[<img src="https://i.imgur.com/W6lFY9k.png">](https://i.imgur.com/W6lFY9k.png)

* ext4
````Bash
mke2fs -t ext4 /dev/xvdb
````

[<img src="https://i.imgur.com/7SL9NGD.png">](https://i.imgur.com/7SL9NGD.png)

#### Mount
````Bash
mount /dev/xvdb /mnt
````
[<img src="https://i.imgur.com/wZBM6eR.png">](https://i.imgur.com/wZBM6eR.png)

[<img src="https://i.imgur.com/3krjGSQ.png">](https://i.imgur.com/3krjGSQ.png)

[<img src="https://i.imgur.com/P76Vnhi.png">](https://i.imgur.com/P76Vnhi.png)


#### Umount
````Bash
umount /mnt
````
[<img src="https://i.imgur.com/Rc1rqbe.png">](https://i.imgur.com/Rc1rqbe.png)

#### Detach Volume
[<img src="https://i.imgur.com/F8xd9xo.png">](https://i.imgur.com/F8xd9xo.png)

[<img src="https://i.imgur.com/LX3QGKu.png">](https://i.imgur.com/LX3QGKu.png)

* State: in-use

[<img src="https://i.imgur.com/UA3bACy.png">](https://i.imgur.com/UA3bACy.png)

* State: available

[<img src="https://i.imgur.com/p2YJYQ3.png">](https://i.imgur.com/p2YJYQ3.png)

* Wrap-up
 * Tag Name : important
   * you can drill down your billing per tags
