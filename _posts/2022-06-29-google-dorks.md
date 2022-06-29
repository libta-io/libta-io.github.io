---
title: "Google Dorks"
header:
toc: true
toc_sticky: true
excerpt_separator:  <!--more-->
categories:
  - Hacking
tags:
  - Google
  - Dorking
  - OSINT
  - Hacking
  - Database
  - Guides
---

<!--more-->

## What is Google Dorks?

Google Dorking, also known as Google hacking, is the method capable of returning the information difficult to locate through simple search queries by providing a search string that uses advanced search operators. 

Primarily, ethical hackers use this method to query the search engine and find crucial information. This Google hacking cheat sheet will help you carry out Google Dorking commands and access hidden information.

When we talk about Google Dorks or Google Hacking, we are referring to advanced search methods on the Google search engine. This method of Internet investigation is based on the principle of OSINT (Open Source Intelligence).

## How to Use Google Dorks?

To use a Google Dork, you simply type in a Dork into the search box on Google and press “Enter”. Here are some of the best Google Dork queries that you can use to search for information on Google.

## Search Operators

**cache**:
```text
* [cache:www.google.com web] will show the cached content with the word “web” highlighted. This functionality is also accessible by clicking on the “Cached” link on Google’s main results page. The query [cache:] will show the version of the web page that Google has in its cache. For instance, [cache:www.google.com] will show Google’s cache of the Google homepage.
```
**link**:
```text
* [link:www.google.com] will list webpages that have links pointing to the Google homepage.
```
**related**:
```text
* [related:www.google.com] will list web pages that are similar to the Google homepage.
```
**info**:
```text
* [info:www.google.com] will show information about the Google homepage.
```
**define**:
```text
* The query [define:] will provide a definition of the words you enter after it, gathered from various online sources. The definition will be for the entire phrase entered (i.e., it will include all the words in the exact order you typed them). Eg: [define:google]
```
**stocks**:
```text
* If you begin a query with the [stocks:] operator, Google will treat the rest of the query terms as stock ticker symbols, and will link to a page showing stock information for those symbols. For instance, [stocks: intc yhoo] will show information about Intel and Yahoo. (Note you must type the ticker symbols, not the company name.)
```
**site**:
```text
* If you include [site:] in your query, Google will restrict the results to those websites in the given domain. For instance, [help site:www.google.com] will find pages about help within www.google.com. [help site:com] will find pages about help within .com urls. Note there can be no space between the “site:” and the domain.
```
**allintitle**:
```text
* If you start a query with [allintitle:], Google will restrict the results to those with all of the query words in the title. For instance, [allintitle: google search] will return only documents that have both “google” and “search” in the title.
```
**intitle**:
```text
* If you include [intitle:] in your query, Google will restrict the results to documents containing that word in the title. For instance, [intitle:google search] will return documents that mention the word “google” in their title, and mention the word “search” anywhere in the document (title or no). Putting [intitle:] in front of every word in your query is equivalent to putting [allintitle:] at the front of your query: [intitle:google intitle:search] is the same as [allintitle: google search].
```
**allinurl**:
```text
* If you start a query with [allinurl:], Google will restrict the results to those with all of the query words in the url. For instance, [allinurl:google search] will return only documents that have both “google” and “search” in the url. Note that [allinurl:] works on words, not url components. In particular, it ignores punctuation. Thus, [allinurl: foo/bar] will restrict the results to page with the words “foo” and “bar” in the url, but won’t require that they be separated by a slash within that url, that they be adjacent, or that they be in that particular word order. There is currently no way to enforce these constraints.
```
**inurl**:
```text
* If you include [inurl:] in your query, Google will restrict the results to documents containing that word in the url. For instance, [inurl:google search] will return documents that mention the word “google” in their url, and mention the word “search” anywhere in the document (url or no). Putting “inurl:” in front of every word in your query is equivalent to putting “allinurl:” at the front of your query: [inurl:google inurl:search] is the same as [allinurl: google search].
```
**filetype**:
```text
* If you include [filetype:] in your query, Google will restrict the results to a certain file format (Word, PDF, Excel, Powerpoint...). For instance, [filetype:PDF google search] will return PDF documents that mention the words "google search" anywhere in the document format that was searched.
```
## Google Dorks Updated Database

```text
Nina Simone intitle:”index.of” “parent directory” “size” “last modified” “description” I Put A Spell On You (mp4|mp3|avi|flac|aac|ape|ogg) -inurl:(jsp|php|html|aspx|htm|cf|shtml|lyrics-realm|mp3-collection) -site:.info
Bill Gates intitle:”index.of” “parent directory” “size” “last modified” “description” Microsoft (pdf|txt|epub|doc|docx) -inurl:(jsp|php|html|aspx|htm|cf|shtml|ebooks|ebook) -site:.info
parent directory /appz/ -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
parent directory DVDRip -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
parent directory Xvid -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
parent directory Gamez -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
parent directory MP3 -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
parent directory Name of Singer or album -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
filetype:config inurl:web.config inurl:ftp
“Windows XP Professional” 94FBR
ext:(doc | pdf | xls | txt | ps | rtf | odt | sxw | psw | ppt | pps | xml) (intext:confidential salary | intext:"budget approved") inurl:confidential
ext:(doc | pdf | xls | txt | ps | rtf | odt | sxw | psw | ppt | pps | xml) (intext:confidential salary | intext:”budget approved”) inurl:confidential
ext:inc "pwd=" "UID="
ext:ini intext:env.ini
ext:ini Version=... password
ext:ini Version=4.0.0.4 password
ext:ini eudora.ini
ext:ini intext:env.ini
ext:log "Software: Microsoft Internet Information Services _._"
ext:log "Software: Microsoft Internet Information
ext:log "Software: Microsoft Internet Information Services _._"
ext:log \"Software: Microsoft Internet Information Services _._\"
ext:mdb inurl:_.mdb inurl:fpdb shop.mdb
ext:mdb inurl:_.mdb inurl:fpdb shop.mdb
ext:mdb inurl:_.mdb inurl:fpdb shop.mdb
filetype:SWF SWF
filetype:TXT TXT
filetype:XLS XLS
filetype:asp DBQ=" _ Server.MapPath("_.mdb")
filetype:asp "Custom Error Message" Category Source
filetype:asp + "[ODBC SQL"
filetype:asp DBQ=" _ Server.MapPath("_.mdb")
filetype:asp DBQ=\" _ Server.MapPath(\"_.mdb\")
filetype:asp “Custom Error Message” Category Source
filetype:bak createobject sa
filetype:bak inurl:"htaccess|passwd|shadow|htusers"
filetype:bak inurl:\"htaccess|passwd|shadow|htusers\"
filetype:conf inurl:firewall -intitle:cvs
filetype:conf inurl:proftpd. PROFTP FTP server configuration file reveals
filetype:dat "password.dat
filetype:dat \"password.dat\"
filetype:eml eml +intext:"Subject" +intext:"From" +intext:"To"
filetype:eml eml +intext:\"Subject\" +intext:\"From\" +intext:\"To\"
filetype:eml eml +intext:”Subject” +intext:”From” +intext:”To”
filetype:inc dbconn
filetype:inc intext:mysql*connect
filetype:inc mysql_connect OR mysql_pconnect
filetype:log inurl:"password.log"
filetype:log username putty PUTTY SSH client logs can reveal usernames
filetype:log “PHP Parse error” | “PHP Warning” | “PHP Error”
filetype:mdb inurl:users.mdb
filetype:ora ora
filetype:ora tnsnames
filetype:pass pass intext:userid
filetype:pdf "Assessment Report" nessus
filetype:pem intext:private
filetype:properties inurl:db intext:password
filetype:pst inurl:"outlook.pst"
filetype:pst pst -from -to -date
filetype:reg reg +intext:"defaultusername" +intext:"defaultpassword"
filetype:reg reg +intext:\"defaultusername\" +intext:\"defaultpassword\"
filetype:reg reg +intext:â? WINVNC3â?
filetype:reg reg +intext:”defaultusername” +intext:”defaultpassword”
filetype:reg reg HKEY* Windows Registry exports can reveal
filetype:reg reg HKEY_CURRENT_USER SSHHOSTKEYS
filetype:sql "insert into" (pass|passwd|password)
filetype:sql ("values _ MD5" | "values _ password" | "values _ encrypt")
filetype:sql (\"passwd values\" | \"password values\" | \"pass values\" )
filetype:sql (\"values _ MD\" | \"values _ password\" | \"values _ encrypt\")
filetype:sql +"IDENTIFIED BY" -cvs
filetype:sql password
filetype:sql password
filetype:sql “insert into” (pass|passwd|password)
filetype:url +inurl:"ftp://" +inurl:";@"
filetype:url +inurl:\"ftp://\" +inurl:\";@\"
filetype:url +inurl:”ftp://” +inurl:”;@”
filetype:xls inurl:"email.xls"
filetype:xls username password email
index of: intext:Gallery in Configuration mode
index.of passlist
index.of perform.ini mIRC IRC ini file can list IRC usernames and
index.of.dcim
index.of.password
intext:" -FrontPage-" ext:pwd inurl:(service | authors | administrators | users)
intext:""BiTBOARD v2.0" BiTSHiFTERS Bulletin Board"
intext:"# -FrontPage-" ext:pwd inurl:(service | authors | administrators | users) "# -FrontPage-" inurl:service.pwd
intext:"#mysql dump" filetype:sql
intext:"#mysql dump" filetype:sql 21232f297a57a5a743894a0e4a801fc3
intext:"A syntax error has occurred" filetype:ihtml
intext:"ASP.NET_SessionId" "data source="
intext:"About Mac OS Personal Web Sharing"
intext:"An illegal character has been found in the statement" -"previous message"
intext:"AutoCreate=TRUE password=_"
intext:"Can't connect to local" intitle:warning
intext:"Certificate Practice Statement" filetype:PDF | DOC
intext:"Certificate Practice Statement" inurl:(PDF | DOC)
intext:"Copyright (c) Tektronix, Inc." "printer status"
intext:"Copyright © Tektronix, Inc." "printer status"
intext:"Emergisoft web applications are a part of our"
intext:"Error Diagnostic Information" intitle:"Error Occurred While"
intext:"Error Message : Error loading required libraries."
intext:"Establishing a secure Integrated Lights Out session with" OR intitle:"Data Frame - Browser not HTTP 1.1 compatible" OR intitle:"HP Integrated Lights-
intext:"Fatal error: Call to undefined function" -reply -the -next
intext:"Fill out the form below completely to change your password and user name. If new username is left blank, your old one will be assumed." -edu
intext:"Generated by phpSystem"
intext:"Generated by phpSystem"
intext:"Host Vulnerability Summary Report"
intext:"HostingAccelerator" intitle:"login" +"Username" -"news" -demo
intext:"IMail Server Web Messaging" intitle:login
intext:"Incorrect syntax near"
intext:"Index of" /"chat/logs"
intext:"Index of /network" "last modified"
intext:"Index of /" +.htaccess
intext:"Index of /" +passwd
intext:"Index of /" +password.txt
intext:"Index of /admin"
intext:"Index of /backup"
intext:"Index of /mail"
intext:"Index of /password"
intext:"Microsoft (R) Windows _ (TM) Version _ DrWtsn32 Copyright (C)" ext:log
intext:"Microsoft CRM : Unsupported Browser Version"
intext:"Microsoft ® Windows _ ™ Version _ DrWtsn32 Copyright ©" ext:log
intext:"Network Host Assessment Report" "Internet Scanner"
intext:"Network Vulnerability Assessment Report"
intext:"Network Vulnerability Assessment Report"
intext:"Network Vulnerability Assessment Report" 本文来自 pc007.com
intext:"SQL Server Driver][SQL Server]Line 1: Incorrect syntax near"
intext:"Thank you for your order" +receipt
intext:"Thank you for your order" +receipt
intext:"Thank you for your purchase" +download
intext:"The following report contains confidential information" vulnerability -search
intext:"phpMyAdmin MySQL-Dump" "INSERT INTO" -"the"
intext:"phpMyAdmin MySQL-Dump" filetype:txt
intext:"phpMyAdmin" "running on" inurl:"main.php"
intextpassword | passcode) intextusername | userid | user) filetype:csv
intextpassword | passcode) intextusername | userid | user) filetype:csv
intitle:"index of" +myd size
intitle:"index of" etc/shadow
intitle:"index of" htpasswd
intitle:"index of" intext:connect.inc
intitle:"index of" intext:globals.inc
intitle:"index of" master.passwd
intitle:"index of" master.passwd 007 电脑资讯
intitle:"index of" members OR accounts
intitle:"index of" mysql.conf OR mysql_config
intitle:"index of" passwd
intitle:"index of" people.lst
intitle:"index of" pwd.db
intitle:"index of" spwd
intitle:"index of" user_carts OR user_cart
intitle:"index.of \*" admin news.asp configview.asp
intitle:("TrackerCam Live Video")|("TrackerCam Application Login")|("Trackercam Remote") -trackercam.com
intitle:(“TrackerCam Live Video”)|(“TrackerCam Application Login”)|(“Trackercam Remote”) -trackercam.com
inurl:admin inurl:userlist Generic userlist files
"'dsn: mysql:host=localhost;dbname=" ext:yml | ext:txt "password:"
"* Authentication Unique Keys and Salts" ext:txt | ext:log
"-- Dumped from database version" + "-- Dumped by pg_dump version" ext:txt | ext:sql | ext:env | ext:log
"-- Dumping data for table `admin`" | "-- INSERT INTO `admin`" "VALUES" ext:sql | ext:txt | ext:log | ext:env
"-- Server version" "-- MySQL Administrator dump 1.4" ext:sql
"DefaultPassword" ext:reg "[HKEY_LOCAL_MACHINESOFTWAREMicrosoftWindows NTCurrentVersionWinlogon]"
"Powered by vBulletin(R) Version 5.6.3"
"System" + "Toner" + "Input Tray" + "Output Tray" inurl:cgi
"The SQL command completed successfully." ext:txt | ext:log
"change the Administrator Password." intitle:"HP LaserJet" -pdf
"define('DB_USER'," + "define('DB_PASSWORD'," ext:txt
"define('SECURE_AUTH_KEY'" + "define('LOGGED_IN_KEY'" + "define('NONCE_KEY'" ext:txt | ext:cfg | ext:env | ext:ini
"index of" "/home/000~ROOT~000/etc"
"index of" inurl:database ext:sql | xls | xml | json | csv
"keystorePass=" ext:xml | ext:txt -git -gitlab
"mailer_password:" + "mailer_host:" + "mailer_user:" + "secret:" ext:yml
"putty.log" ext:log | ext:cfg | ext:txt | ext:sql | ext:env
"secret_key_base:" ext:exs | ext:txt | ext:env | ext:cfg
/etc/certs + "index of /" */*
/etc/config + "index of /" /
AXIS Camera exploit
Index of /_vti_pvt +"*.pwd"
Server: Mida eFramework
allintext:"Copperfasten Technologies" "Login"
allintext:"Index Of" "cookies.txt"
allintext:@gmail.com filetype:log
ext:php intitle:phpinfo "published by the PHP Group"
ext:sql | ext:txt intext:"-- phpMyAdmin SQL Dump --" + intext:"admin"
ext:txt | ext:log | ext:cfg "Building configuration..."
ext:txt | ext:log | ext:cfg | ext:yml "administrator:500:"
ext:yml | ext:txt | ext:env "Database Connection Information Database server ="
intext:"Connection" AND "Network name" AND " Cisco Meraki cloud" AND "Security Appliance details"
intext:"Healthy" + "Product model" + " Client IP" + "Ethernet"
intext:"Incom CMS 2.0"
intext:"SonarQube" + "by SonarSource SA." + "LGPL v3"
intext:"user name" intext:"orion core" -solarwinds.com
intext:construct('mysql:host
intitle:"Agent web client: Phone Login"
intitle:"Exchange Log In"
intitle:"Humatrix 8"
intitle:"Insurance Admin Login" | "(c) Copyright 2020 Cityline Websites. All Rights Reserved." | "http://www.citylinewebsites.com"
intitle:"NetCamSC*"
intitle:"NetCamSC*" | intitle:"NetCamXL*" inurl:index.html
intitle:"NetCamXL*"
intitle:"Please Login" "Use FTM Push"
intitle:"Powered by Pro Chat Rooms"
intitle:"Sphider Admin Login"
intitle:"Xenmobile Console Logon"
intitle:"index of" "*.cert.pem" | "*.key.pem"
intitle:"index of" "*Maildir/new"
intitle:"index of" "/.idea"
intitle:"index of" "/xampp/htdocs" | "C:/xampp/htdocs/"
intitle:"index of" "Clientaccesspolicy.xml"
intitle:"index of" "WebServers.xml"
intitle:"index of" "anaconda-ks.cfg" | "anaconda-ks-new.cfg"
intitle:"index of" "config.exs" | "dev.exs" | "test.exs" | "prod.secret.exs"
intitle:"index of" "credentials.xml" | "credentials.inc" | "credentials.txt"
intitle:"index of" "db.properties" | "db.properties.BAK"
intitle:"index of" "dump.sql"
intitle:"index of" "filezilla.xml"
intitle:"index of" "password.yml
intitle:"index of" "service-Account-Credentials.json" | "creds.json"
intitle:"index of" "sitemanager.xml" | "recentservers.xml"
intitle:"index of" intext:"apikey.txt
intitle:"index of" intext:"web.xml"
intitle:"index of" intext:credentials
intitle:"index of" inurl:admin/download
intitle:"irz" "router" intext:login gsm info -site:*.com -site:*.net
intitle:"web client: login"
intitle:("Index of" AND "wp-content/plugins/boldgrid-backup/=")
intitle:Login intext:HIKVISION inurl:login.asp?
intitle:index of .git/hooks/
USG60W|USG110|USG210|USG310|USG1100|USG1900|USG2200|"ZyWALL110"|"ZyWALL310"|"ZyWALL1100"|ATP100|ATP100W|ATP200|ATP500|ATP700|ATP800|VPN50|VPN100|VPN300|VPN000|"FLEX")
jdbc:mysql://localhost:3306/ + username + password ext:yml | ext:javascript -git -gitlab
jdbc:oracle://localhost: + username + password ext:yml | ext:java -git -gitlab
jdbc:postgresql://localhost: + username + password ext:yml | ext:java -git -gitlab
jdbc:sqlserver://localhost:1433 + username + password ext:yml | ext:java
site:*gov.* intitle:index.of db
site:checkin.*.* intitle:"login"
site:ftp.*.*.* "ComputerName=" + "[Unattended] UnattendMode"
site:gov ext:sql | ext:dbf | ext:mdb
site:password.*.* intitle:"login"
site:portal.*.* intitle:"login"
site:sftp.*.*/ intext:"login" intitle:"server login"
site:user.*.* intitle:"login"
ssh_host_dsa_key.pub + ssh_host_key + ssh_config = "index of / "
```

## Special search string to find vulnerable websites

```text
inurl:php?=id1
inurl:index.php?id=
inurl:trainers.php?id=
inurl:buy.php?category=
inurl:article.php?ID=
inurl:play_old.php?id=
inurl:declaration_more.php?decl_id=
inurl:pageid=
inurl:games.php?id=
inurl:page.php?file=
inurl:newsDetail.php?id=
inurl:gallery.php?id=
inurl:article.php?id=
inurl:show.php?id=
inurl:staff_id=
inurl:newsitem.php?num= andinurl:index.php?id=
inurl:trainers.php?id=
inurl:buy.php?category=
inurl:article.php?ID=
inurl:play_old.php?id=
inurl:declaration_more.php?decl_id=
inurl:pageid=
inurl:games.php?id=
inurl:page.php?file=
inurl:newsDetail.php?id=
inurl:gallery.php?id=
inurl:article.php?id=
inurl:show.php?id=
inurl:staff_id=
inurl:newsitem.php?num=
inurl: 1051/viewer/live/index.html?lang=en
inurl: inurl:"view.shtml" ext:shtml
inurl:"/?q=user/password/"
inurl:"/cgi-bin/guestimage.html" "Menu"
inurl:"/php/info.php" "PHP Version"
inurl:"/phpmyadmin/user_password.php
inurl:"servicedesk/customer/user/login"
inurl:"view.shtml" "Network"
inurl:"view.shtml" "camera"
inurl:"woocommerce-exporter"
inurl:/?op=register
inurl:/Jview.htm + "View Video - Java Mode"
inurl:/Jview.htm + intext:"Zoom :"
inurl:/adfs/ls/?SAMLRequest
inurl:/adfs/ls/idpinitiatedsignon
inurl:/adfs/oauth2/authorize
inurl:/cgi-bin/manlist?section
inurl:/eftclient/account/login.htm
inurl:/homej.html?
inurl:/index.html?size=2&mode=4
inurl:/pro_users/login
inurl:/wp-content/themes/altair/
inurl:/xprober ext:php
inurl:RichWidgets/Popup_Upload.aspx
inurl:Sitefinity/Authenticate/SWT
inurl:adfs inurl:wctx inurl:wtrealm -microsoft.com
inurl:authorization.ping
inurl:https://trello.com AND intext:@gmail.com AND intext:password
inurl:idp/Authn/UserPassword
inurl:idp/prp.wsf
inurl:login.seam
inurl:nidp/idff/sso
inurl:oidc/authorize
inurl:opac_css
inurl:weblogin intitle:("USG20-VPN"|"USG20W-VPN"|USG40|USG40W|USG60|
```

## How to safeguard information from Google Dorks?

**You can take the following safety measures to protect your information from being disclosed by google dorks**:
* Protect pages that contain sensitive information via username and password.
* Run regular dork queries against your website to discover the sensitive information.
* Request removal of sensitive information if found via google search console
https://support.google.com/webmasters/answer/9689846?hl=en&visit_id=637871614748203924-38706967&rd=1
* Block sensitive content by using a robots.txt file located in your root-level website directory.

**Note**:
Google Search is very useful as well as equally harmful at the same time. Because it indexes everything available over the web.

You can also follow appropriate security mechanisms and prevent systems from exposing sensitive data. Follow [OWASP](https://owasp.org/), which provides a standard awareness document for developers and web application security.

[Scraper API](https://www.scraperapi.com/?fp_ref=box-piper-app) provides a proxy service designed for web scraping. With over 20 million residential IPs across 12 countries, as well as software that can handle JavaScript rendering and solving CAPTCHAs, you can quickly complete large scraping jobs without ever having to worry about being blocked by any servers.


## Conclusion

Google Search Engine is designed to crawl anything over the internet and this helps us to find images, text, videos, news and plethora of information sources. With it’s tremendous capability to crawl, it indexes data along the way, which also includes sensitive information like email addresses, login credentials, sensitive files, website vulnerabilities, and even financial information.

A Google Dork is a search query that looks for specific information on Google’s search engine. Google Dorks are developed and published by hackers and are often used in “Google Hacking”.

Google Dorks are extremely powerful. They allow you to search for a wide variety of information on the internet and can be used to find information that you didn’t even know existed.

Because of the power of Google Dorks, they are often used by hackers to find information about their victims or to find information that can be used to exploit vulnerabilities in websites and web applications.

> Google Dork is a search query we give to Google to search for more granular information and quickly retrieve relevant information. For example, try searching for your name and check the results with a search query [inurl:your-name]. Analyze the difference. You just asked Google to do a more in-depth search and it did.

Google search service is never intended to gain unauthorised access of data but nothing can be done if we ourselves kept data in the open and do not follow proper security mechanisms.

Essentially emails, username, passwords, financial data and etc. shouldn’t be available in public until and unless it’s meant to be. Example, our details with the bank are never expected to be available in a google search. But our social media details are available in public because we ourselves allowed it.

**Disclaimer**:
This article is written to provide relevant information only and is for educational purposes. Confidentiality and data security must always be respected.

Thanks for reading!