# Apache_Pig
Big data project using Apache Pig

## Team members Names:
1. Sushma Yedugani
1. Nikitha Kethireddy
1. Deepthi Tejaswani Chokka
1. Deepak Malempati

## Team Members GitHub profile links:
1. https://github.com/sushma95
1. https://github.com/nikithakethireddy1996
1. https://github.com/Deepthi1003
1. https://github.com/Deepakmalempati

## Team Members Images:
<img src="https://github.com/nikithakethireddy1996/apache_pig/blob/master/WhatsApp%20Image%202020-05-24%20at%206.55.23%20PM.jpeg" width="200" height="300"/> <img src=https://github.com/nikithakethireddy1996/apache_pig/blob/master/IMG-2723.jpg width="200" height="300"/> <img src=https://github.com/nikithakethireddy1996/apache_pig/blob/master/WhatsApp%20Image%202020-05-24%20at%207.26.21%20PM.jpeg width="200" height="300"/> <img src= https://github.com/nikithakethireddy1996/apache_pig/blob/master/WhatsApp%20Image%202020-05-24%20at%207.47.43%20PM.jpeg
 width="200" height="300"/> 
 
## Introduction to Apache-Pig:
Apache Pig is a platform for analyzing large data sets that consists of a high-level language for expressing data analysis programs, coupled with infrastructure for evaluating these programs. The salient property of Pig programs is that their structure is amenable to substantial parallelization, which in turns enables them to handle very large data sets.<br>

## Features of Apache-Pig:
#### ```Rich set of operators :``` <br>
Apache pig has a rich collection set of operators in order to perform operations like join, filer, and sort.
#### ```Ease of Programming :``` <br>
Pig Latin is similar to SQL so it is very easy for developers to write a Pig script. If we have knowledge of SQL language, then it is very easy to learn Pig Latin language as it is similar to SQL language.
#### ```Optimization opportunities :``` <br> 
In Apache pig has automatically optimized  execution of the task gets by itself, hence the programmers need to focus only on the semantics of the language.
#### ```Extensibility :``` <br> 
Using the existing operators in Apache pig, users can develop their own functions to read, process, and write data.
#### ```User Define Functions :``` <br>
Apache Pig provides the facility to create User-defined Functions easily in other language like java then invoke them in PigLatin Scripts.
#### ```ETL (Extract Transform Load) :``` <br>
Apache Pig extracts the huge data set, performs operations on huge data and dumps the data in the required format in HDFS.

## Applications of Apache-Pig:
* It is used to process huge data sources like web logs, streaming online data etc.
* It Support Ad Hoc queries across large data set.
* Used to perform data processing in search platforms.
* It is also used to process time sensitive data loads.
* Apache Pig is generally used by data scientists for performing tasks like ad-hoc processing and quick prototyping.

## Installation steps of Apache-Pig:
1. Download Apache Pig from http://apache.mirrors.lucidnetworks.net/pig/pig-0.17.0/ (file to download: pig-0.17.0.tar.gz)
1. Copy the file to C drive.
1. Open Powershell in C drive and unzip the downloaded file using <br>
```tar -xzvf pig-0.17.0.tar.gz```
1. pig-0.17.0 folder will be created.
1. Set Below paths in environment variables
     ```
     PIG_HOME - C:\pig-0.17.0
     Path - %PIG_HOME%\bin
     ```
1. open the file pig.cmd(From bin directory of PIG) using vscode   
    - look for the line <br>
    ```set HADOOP_BIN_PATH=%HADOOP_HOME%\bin```    
    - replace this with <br>
    ```set HADOOP_BIN_PATH=%HADOOP_HOME%\libexec``` 
1. To verify installation run the following command using powershell <br>
    ```pig --version``` 
          or
    ```pig -version```
    
## Apache Pig commands executed by Deepak
1. Steps to run Apache Pig in local mode  
   ```pig -x local```
1. Command to load new dataset into pig
```
netflix_list = LOAD 'input.txt' using PigStorage(',')
AS
(show_id:chararray,type:chararray,title:chararray,director:chararray,cast:chararray,country:chararray,date_added:chararray,release_year:chararray,rating:chararray,duration:chararray,listed_in:chararray);
```
1. Command to retrive only ID, Title and duration coulmns from the dataset
```
foreachlist = foreach netflix_list generate show_id, title, duration;
```
1. Command to display the output in the grunt console.
```
dump foreachlist;
```
1. Command to arrange movies list by shortest duration
```
grouping = group foreachlist by duration;

lowest_duration = foreach grouping generate group, MIN(foreachlist.duration);
dump lowest_duration;
```
## References:
1. https://beyondcorner.com/learn-apache-pig-tutorials/features-application-apache-pig/
1. https://www.youtube.com/watch?v=DabelKGxsM4&feature=youtu.be
 
