If you forget your password on iPython Notebook then ...

1. access your ec2 instance. 

2. Create a new password hash using the following commands:
ipython
In [1]:from IPython.lib import passwd
In [2]:passwd()

3. Copy-paste the new hashed password in your ipython/jupyter notebooks config file.



REFERENCES
==========
http://blog.impiyush.me/2015/02/running-ipython-notebook-server-on-aws.html
