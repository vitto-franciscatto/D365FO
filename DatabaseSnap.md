# Database snapshot to keep cenario for debbuging purposes

## Create snapshot

```
CREATE DATABASE AxDB_Snapshot ON
(Name ='AxDB_16042026', -- this is Data file name from database properties
FileName='J:\Snapshots\AxDB.snp') -- ensure the drive has enough space to store the database
AS SNAPSHOT OF AxDB;
```

## Restore snapshot

```
USE MASTER 

ALTER DATABASE AxDB SET SINGLE_USER WITH ROLLBACK IMMEDIATE

RESTORE DATABASE AxDB from DATABASE_SNAPSHOT = 'AxDB_Snapshot'

ALTER DATABASE AxDB SET MULTI_USER
```
