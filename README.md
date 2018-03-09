# rnovo-snap
rnovo-snap

Log

[March 8th, 2018]
[19:45]

Strategy 

* Mount environment vbox 
* Download Sql 2012 
  - started at 19:45
* Download Windows 2012 R2 
  - started at 19:45
* Write here some more 
* Update T7 to fit 


VBox Machine Creation 

> vboxmanage aliases and shortcut functions from [T7](http://github.com/msant77/t7) github repository are used from these part of the lab

```
curl -s http://github.com/msant77/t7/master/bashrc/.bash_vbox >> .t7lvb
source .t7lvb

t7act vb
vbcreate sqlsnap1 5 20 WindowsNT_64


## Attempts on Sql Server 2014

The following situations halt undefinitely: 

- Execution of the command: 
```
CREATE DATABASE AdventureWorks_dbss1800 ON
( NAME = AdventureWorks, FILENAME = 
'C:\Program Files\Microsoft SQL Server\MSSQL12.MSSQLSERVER\MSSQL\DATA\AdventureWorks_data_1800.ss' )
AS SNAPSHOT OF AdventureWorks;
GO
```
In here, even trying to cancel the command after command oblivion keeps the interface halted.
No entries are found on Sql Profile. 
No entries are found at Event Viewer.

- Running the debug mode of the sql snap tool (in this case there is still hope for stoping the execution by either stopping debug at Visual Studio 2015 or hitting Control-C at the terminal)
No entries are found at Event Viewer
- TODO: Test Sql Profile



## Reference

[Back up and Restore of SQL Server Databases](https://msdn.microsoft.com/en-us/library/ms187048(v=sql.110).aspx)

- Looked for discontinuation or deprecation of the snapshot and backup to virtual device on the following Sql Server versions (considering the 2005 version the one with more documetation on the matter): 
  - Sql Server 2012 (done) - 21:50 2018/02/08
  - Sql Server 2008 (on)

- Look for the extensive documentation at the link above
  = 
