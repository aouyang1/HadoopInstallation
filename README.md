# 1. Install the boto package for python
This will allow you to programatically interface with your AWS account
```
$ sudo pip install boto
```
Create a .boto file in your home directory
```
$ touch ~/.boto
```
Insert the following into .boto with your AWS credentials. These credentials will be used to access you AWS cluster as well as AWS's S3 storage.
```
[Credentials]
aws_access_key_id = XXXXXX
aws_secret_access_key = XXXXX+XXXX
```
# 2. Clone repository
* Place in home folder
* Move into the HadoopInstallation folder
```
$ git clone https://github.com/aouyang1/HadoopInstallation.git
$ cd HadoopInstallation
```
## Hadoop Installation
```
$ ./install_hadoop.sh ~/.ssh/<personal.pem> <region> <cluster-name>
```
You will need to SSH into the Namenode and start Hadoop after installation
```
$ $HADOOP_HOME/sbin/start-dfs.sh
$ $HADOOP_HOME/sbin/start-yarn.sh
$ $HADOOP_HOME/sbin/mr-jobhistory-daemon.sh start historyserver
```
