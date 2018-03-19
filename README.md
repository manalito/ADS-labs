# ADS-labs

## Labo 2

#### Answers
1. How many log entries are in the file? : 
`wc -l ads_website.log`  
Response: 2781

2. How many accesses were successful (server sends back a status of 200) 
and how many had an error of "Not Found" (status 404)?  
`cat ads_website.log | cut -f10 | grep 200 | wc -l`  
`cat ads_website.log | cut -f10 | grep 404 | wc -l`  
Responses:  
200: 1610
400: 21


What are the URIs that generated a "Not Found" response? 
Be careful in specifying the correct search criteria: avoid selecting lines 
that happen to have the character sequence 404 in the URI.

How many different days are there in the log file on which requests were made?

How many accesses were there on 4th March 2014?

Which are the three days with the most accesses? 
Hint: Create first a pipeline that produces a list of dates preceded by the count of log entries on that date.

Which is the user agent string with the most accesses?

If a web site is very popular and accessed by many people the user agent strings appearing in the server's log 
can be used to estimate the relative market share of the users' computers and operating systems. 
How many accesses were done from browsers that declare that they are running on Windows, Linux and Mac OS X?

Read the documentation for the tee command. Repeat the analysis of the previous question for browsers running 
on Windows and insert tee into the pipeline such that the user agent strings (including repeats) are written 
to a file for further analysis (the filename should be useragents.txt). What are the operating systems Windows NT 6.1, 6.2 and 6.3?

