# Hands-on Lab 1: HDFS 

## Objective:
- Transfer IN/OUT files between local file-system and HDFS
-	Files Management on HDFS
-	Manipulate file on HDFS

## Login to Virtual Machine on VMware
```
Username: testuser
Password: testuser
```
Open the new terminal and follow the below instruction. (See Hadoop Cheat sheet for the Hadoop command detail.)

## 0) start HDFS Service
```
$ start-dfs.sh
$ start-yarn.sh
```

## 1) Upload dataset to HDFS

```
$ hadoop fs -put LogAnalyzer.log
```
