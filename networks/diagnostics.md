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
    
