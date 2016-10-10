Meteor 1.4 on Windows 10 
------------------------
```sh
   meteor update
   meteor npm rebuild
```

See [migrating to meteor 1.4](https://guide.meteor.com/1.4-migration.html)
   
If you get [node-gyp errors](https://forums.meteor.com/t/node-gyp-rebuild-installation-error-when-adding-a-package-to-meteor-app-in-windows-7/7410/2):
https://github.com/nodejs/node-gyp

Install all the required tools and configurations using Microsoft's windows-build-tools using 
```sh
   npm install --global --production windows-build-tools 
```
from an elevated PowerShell or CMD.exe (run as Administrator).


Set up environment variables in the Advanced System Settings.


There are build issues on Windows.  A workaround is to build on Linux and to do a file transfer via Github or Dropbox.  The key idea is that Node will run on any operating system.
