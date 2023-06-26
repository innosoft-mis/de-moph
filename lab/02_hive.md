# Lab 2: Hive

ใช้ไฟล์ /user/testuser/hospcode_dataset/data.csv ใน hdfs ที่ได้จาก lab 1

## 0) Start HDFS & Yarn

```
start-dfs.sh && start-yarn.sh
```

## 1) 

```
hive
```

## 2)

```
CREATE EXTERNAL TABLE IF NOT EXISTS hospcode (
  hospcode INT,
  name STRING,
  address STRING,
  moopart STRING,
  tmbpart STRING,
  amppart STRING,
  chwpart STRING,
  area_code STRING,
  tmbpart_text STRING,
  amppart_text STRING,
  chwpart_text STRING,
  zipcode STRING,
  hosptype STRING,
  hosptype_text STRING,
  sss_code STRING,
  sss_code_text STRING,
  hospital_phone STRING,
  hospital_fax STRING,
  date_report STRING,
  date_update STRING)
ROW FORMAT DELIMITED
FIELDS TERMINATED BY ','
STORED AS TEXTFILE
location '/user/testuser/hospcode_dataset';
```

## 3)

```
SELECT * FROM hospcode LIMIT 3;
```

## 4) 

```
exit
```

## 5)

```
hiveserver2
```

## 6)
```
beeline -u jdbc:hive2://localhost:10000 -n testuser
```

## 5)
```
!quit
```
