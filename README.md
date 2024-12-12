                                        Highly scalable web application


1.To  test scalable web application https://blog.harishc.site/ we  are using wordpress installed as a blog using apache web server in autoscaling with application load balancer and database is installed in Rds

2.Using cli as testing tool i am using apache benchmark and siege as testing tool for increasing load on server

siege -c 10 -r 100 -d 1 http://blog.harishc.site ,
ab -n 100000 -c 10 http://blog.harishc.site//

3.For load conditions i kept if cpu usage is greater than 10 and 10 seconds to warm up as if cpu usage crosses 10 percentage more that 10 seconds new instances count will be increasing 

4.During load testing cpu increased above 90 percentage and application  load balancer is getting 3.5 requests

5.So instances count increased from 1 to 10 due to load 


