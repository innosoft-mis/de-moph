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
และทำการ Download ไฟล์ hospcode.csv จาก URL ที่วิทยากรแจ้ง

Open the new terminal and follow the below instruction. (See Hadoop Cheat sheet for the Hadoop command detail.)

## 0) start HDFS Service
```
$ start-dfs.sh
$ start-yarn.sh
```

## 1) Upload dataset to HDFS

```
$ hadoop fs -put ~/Downloads/hospcode.csv
```

## 2)	List file on HDFS, explain the difference result between -ls and -lsr

```
$ hadoop fs –ls
$ hadoop fs -lsr 
```

## 3)	Create directory on HDFS, and move file into created directory.

```
$ hadoop fs -mkdir hospcode_dataset
$ hadoop fs -mv /user/testuser/hospcode.csv /user/testuser/hospcode_dataset
```

Rename the hospcode file
```
$ hadoop fs -mv /user/testuser/hospcode_dataset/hospcode.csv /user/testuser/hospcode_dataset/data.csv
```

## 4)	Display contents of hospcode.csv file

Display All Content in the terminal
```
$ hadoop fs -cat /user/testuser/hospcode_dataset/data.csv
```

Display only few head line
```
$ hadoop fs -cat /user/testuser/hospcode_dataset/data.csv | head
```

Display only few tail line
```
$ hadoop fs -cat /user/testuser/hospcode_dataset/data.csv | tail
```

Display last 1k byte of file 
```
$ hadoop fs -tail /user/testuser/hospcode_dataset/data.csv
```
