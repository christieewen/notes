When creating a development server "instance" from a production "snapshot" remember there may be running processes you don't care about in development.
Resources get used up very quickly and can get costly.
Calculate costs here:
http://calculator.s3.amazonaws.com/index.html

Make sure to kill those processes.

For example:
* service upstartname stop
* service nginx stop
* kill "mongodb process id"


Best practice: 
* Don't autoscale your database server. Be sure to separate your database server to another instance.
* Use opensource script to do a weekly "snapshot" of all the instances.

To grow your server, you'll change the instance type on the instance.

