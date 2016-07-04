Trouble Shooting
================


Sometimes errors occur when your node app is already running.  You can check by typing:
  
  ps -aux | grep node


If your development server is not on your local machine.  For example, your development server is an AWS EC2 instance then you'll
need to change the host and port settings in your node application.
Port issues can be a setting in your node application.  Check where the port is being set in app.js

127.0.0.1 which is the default localhost setting will not work with AWS EC2 if you want to access it from a browser.  
You can either open it up to the world 0.0.0.0 or put in a specific value in your app.js

For example:
Instead of:
  app.listen('6001', '127.0.0.1')
Do this:
  app.listen('6001')
  
  
  
Check your node and npm version as well.
To upgrade node via npm:
http://tecadmin.net/upgrade-nodejs-via-npm/#
