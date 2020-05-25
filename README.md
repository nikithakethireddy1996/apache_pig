# apache_pig
Big data project using Apache_Pig

## Installtion steps
1. download Apache Pig from http://apache.mirrors.lucidnetworks.net/pig/pig-0.17.0/ (file to download: pig-0.17.0.tar.gz)
1. Copy the file to C drive.
1. Open Powershell in C drive and unzip the downloaded file using ```tar -xzvf pig-0.17.0.tar.gz```
pig-0.17.0 folder will be created
1. Set Below paths in environment variables
```
PIG_HOME - C:\pig-0.17.0
Path - %PIG_HOME%\bin
```
1. open the file pig.cmd(From bin directory of PIG)   
   look for the line set HADOOP_BIN_PATH=%HADOOP_HOME%\bin    
   replace this with set HADOOP_BIN_PATH=%HADOOP_HOME%\libexec 
1. To verify installation run ```pig - version``` using powershell
