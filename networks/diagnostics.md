To see changes to your website when changing DNS, from the cmd console on a local Windows machine type:

    ipconfig /flushdns


To check on your server, type:

    ping yourdomain.com
    

To see what connections are established, type:
    
    netstat -petune

Other:
    netstat -an | grep <keyword>

To reload nginx (reload is an elegant feature of nginx where all workers and jobs get finished before restarting):

    sudo service nginx reload
    

Look at the error message.  Check logs
Example:
    more /var/logs/<kibana.stderr>
    
It turned out chmod +R fixed the problem where there was a apt-get bug.  The error message did say that the file was not accessible.
