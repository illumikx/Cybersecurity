# Open Source Intelligence Gathering

> Open Source Intelligence or OSINT is sort of your first method into gathering information about a client, website, or target. It's considered a passive way to gather information as your not actually interacting with the network / website but rather gathering information from a third party. Luckily there are a lot of tools that are able to assist in this process. Such as Search enginges, Goog-mail.py, API's, and more.

## OSINT Tools

* [Scripts](#Scripts)
* [Google Dorking and Shadow Files](#Google-Dorking-and-Shadow-Files)


### Scripts

The script that i'm using is Goog-mail.py. This script is an automated way to search google for email addresses. As with any script that you might find yourself downloading off the internet, make sure to read the source code to know exactly what it's doing and if it could potentially harm your computer.  By using Goog-mail.py you can target a specific domain. In this example the target is Uk arm of IBM. if we type in uk.ibm.com in our script it would scrape information based on the uk.ibm.com domain we specficed. You can then save this document, and use later as it could be helpful for phsing emails and other malware entrypoints. It's also important to verify the information gathered by the script manually as some of it can be outdated.


### Google Dorking and Shadow Files

Google like any other search engine is a valuable tool when trying to come across information about a target. It's encouraged to use multiple search engines to try and uncover as much information as you can. Google Dorking can help identify vulnerable sites and data and it can be fairly simple. for example try typing in this into google
  ```powershell
    inurl:/etc/passwd root:x:0:0:root:/root:/bin/bash
  ```
If you come across a website while using this it points toa insecurely configured Linux or UNIX Host. This file contains information such as usernames for the system. It used to contain both usernames and password however Password hashes are now stored in the shadow files.
Note it is very important that if you do come across an exposed website do not click on it, as this can be viewed as you trying to hack into the system. This could land you in legal scrutinity if you don't have permission/

   Another thing you can use in google is 
  ```powershell
    filetype:doc inurl:gov intext:"default password"
  ```
  This targets word document types ( you can change the filetype to txt. pdf or anything you desire) and its looking only a .gov sites copntainting text for default passwords. This can be very usefult to grab a list of default passwords easily
