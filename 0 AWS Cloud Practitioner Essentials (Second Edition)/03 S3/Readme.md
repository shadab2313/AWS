# S3

## Acronym
* S3 - Simple Storage Service

* AWS Console\Services\S3

[<img src="https://i.imgur.com/iIMF2sW.png">](https://i.imgur.com/iIMF2sW.png)

   * What is S3 ?
      * Managed cloud storage service
      * Store virtually unlimited number of objects
   * E.g.
      * media/welcome.mp4

[<img src="https://i.imgur.com/3Egndsc.png">](https://i.imgur.com/3Egndsc.png)

[<img src="https://i.imgur.com/9RkCQTQ.png">](https://i.imgur.com/9RkCQTQ.png)

* Access
   * AWS Management Console
   * AWS CLI
   * AWS SDKs

* E.g. Object (buck)

[<img src="https://i.imgur.com/IPS9c0u.png">](https://i.imgur.com/IPS9c0u.png)

* Use Cases
   * Storing Application Assets
   * Static Web Hosting
   * Backup & Disaster Recovery
   * Staging area for Big Data
   * and so on

* Demo
   * Create a bucket

[<img src="https://i.imgur.com/6aZybkS.png">](https://i.imgur.com/6aZybkS.png)

   * Name & region
      * NB: Bucket name must not contain uppercase characters
      
[<img src="https://i.imgur.com/RDtshAe.png">](https://i.imgur.com/RDtshAe.png)
[<img src="https://i.imgur.com/6GiQsXB.png">](https://i.imgur.com/6GiQsXB.png)

````Bach
cat demot.txt
````
[<img src="https://i.imgur.com/k4gTZ2o.png">](https://i.imgur.com/k4gTZ2o.png)
* Goal : To Copy this file over to my S3 bucket
````Bash
aws s3 cp 
````
