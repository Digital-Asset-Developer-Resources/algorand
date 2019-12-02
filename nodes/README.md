## Nodes

* [public net]()  

* [testnet]()  

* [mainnet](AWS AMI)


### Install from AWS AMI

* Step thru [VPC notebook](https://github.com/Digital-Asset-Developer-Resources/aws/blob/master/VPC.ipynb)

  * Notice the VPC id, subnet id and security group id for AMI launch.  
  
* Search and select the public AMI:  

![AMI](https://github.com/Digital-Asset-Developer-Resources/algorand/blob/master/images/AWS%20AMI%201.png)  
  
* Select the desired Instance Tier:  

![Instance Tier](https://github.com/Digital-Asset-Developer-Resources/algorand/blob/master/images/AWS%20AMI%202.png)  

* Select the VPC and subnet IDs:  

![VPC/Subnet IDs](https://github.com/Digital-Asset-Developer-Resources/algorand/blob/master/images/AWS%20AMI%203a.png)  

* Update the USER DATA to automount the chain data:  

![mount chain data](https://github.com/Digital-Asset-Developer-Resources/algorand/blob/master/images/AWS%20AMI%203b.png)  

* Set a Name Tag to label instance on EC2 console  
  
![Set Name Tag](https://github.com/Digital-Asset-Developer-Resources/algorand/blob/master/images/AWS%20AMI%204.png)  
  
* Select the security group ID:  

![Select Security Group](https://github.com/Digital-Asset-Developer-Resources/algorand/blob/master/images/AWS%20AMI%205.png)  
* Review and launch new instance:  

![Launch Instance](https://github.com/Digital-Asset-Developer-Resources/algorand/blob/master/images/AWS%20AMI%206.png)  





### Scaffolding  

ubuntu@123.456.789.0:/data/algorand.com$ ls -lt  

drwxrwxr-x 7 ubuntu ubuntu      334 Nov 25 15:18 betanetdata  
-rwxrwxr-x 1 ubuntu ubuntu 25751598 Nov 25 15:16 updater  
-rwxrwxr-x 1 ubuntu ubuntu 16426300 Nov 25 15:16 node_exporter  
-rwxrwxr-x 1 ubuntu ubuntu      582 Nov 25 15:16 sudoers.template  
-rwxrwxr-x 1 ubuntu ubuntu      583 Nov 25 15:16 systemd-setup.sh  
-rwxrwxr-x 1 ubuntu ubuntu    14932 Nov 25 15:16 update.sh  
-rwxrwxr-x 1 ubuntu ubuntu 13852626 Nov 25 15:16 msgpacktool  
-rwxrwxr-x 1 ubuntu ubuntu 26503296 Nov 25 15:16 kmd  
-rwxrwxr-x 1 ubuntu ubuntu 33939128 Nov 25 15:16 goal  
-rwxrwxr-x 1 ubuntu ubuntu 21622707 Nov 25 15:16 diagcfg  
-rwxrwxr-x 1 ubuntu ubuntu      249 Nov 25 15:16 find-nodes.sh  
-rwxrwxr-x 1 ubuntu ubuntu 27372168 Nov 25 15:16 catchupsrv  
-rwxrwxr-x 1 ubuntu ubuntu     4331 Nov 25 15:16 ddconfig.sh  
-rwxrwxr-x 1 ubuntu ubuntu  3009442 Nov 25 15:16 carpenter  
-rwxrwxr-x 1 ubuntu ubuntu 25258688 Nov 25 15:16 algokey  
-rw-rw-r-- 1 ubuntu ubuntu     1389 Nov 25 15:16 algorand@.service.template  
-rwxrwxr-x 1 ubuntu ubuntu 28088304 Nov 25 15:16 algoh  
-rwxrwxr-x 1 ubuntu ubuntu 32599800 Nov 25 15:16 algod  
-rwxrwxr-x 1 ubuntu ubuntu 14530034 Nov 25 15:16 algocfg  
-rw-rw-r-- 1 ubuntu ubuntu    36469 Nov 25 15:16 COPYING  
drwxrwxr-x 2 ubuntu ubuntu       87 Nov 25 15:16 backup  
drwxrwxr-x 7 ubuntu ubuntu      100 Nov 25 15:16 genesisfiles  
  

. [betanet]()  

ubuntu@123.456.789.0:/data/algorand.com/betanetdata$ ls -lt  

-rw-rw-r-- 1 ubuntu ubuntu 1004634162 Nov 25 20:50 agreement.cdv  
-rw-rw-r-- 1 ubuntu ubuntu  155810311 Nov 25 20:50 node.log  
drwx------ 2 ubuntu ubuntu        258 Nov 25 15:18 betanet-v1.0  
-rw------- 1 ubuntu ubuntu        366 Nov 25 15:18 algod-out.log  
-rw-r--r-- 1 ubuntu ubuntu         15 Nov 25 15:18 algod.net  
-rw-r--r-- 1 ubuntu ubuntu          5 Nov 25 15:18 algod.pid  
-rw------- 1 ubuntu ubuntu          0 Nov 25 15:18 algod.lock  
-rw-r--r-- 1 ubuntu ubuntu         64 Nov 25 15:18 algod.token  
-rw------- 1 ubuntu ubuntu          0 Nov 25 15:18 algod-err.log  
-rw-rw-r-- 1 ubuntu ubuntu       1633 Nov 25 15:18 config.json  
drwx------ 3 ubuntu ubuntu        145 Nov 25 15:17 kmd-v0.5  
-rw-rw-r-- 1 ubuntu ubuntu       8859 Nov 25 15:17 genesis.json  
drwx------ 2 ubuntu ubuntu          6 Nov 25 15:16 goal.cache  
drwxrwxr-x 2 ubuntu ubuntu          6 Nov 25 15:16 devnet-v1.0  
-rw-rw-r-- 1 ubuntu ubuntu         12 Nov 25 15:16 wallet-genesis.id  
-rw-rw-r-- 1 ubuntu ubuntu       1634 Nov 25 15:16 config.json.example  
drwxrwxr-x 2 ubuntu ubuntu         37 Nov 25 15:16 backup  
