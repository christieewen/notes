Following is a list of few important Linux/Unix commands

cat -- Display file contents

chgrp -- Change file group

chmod -- Change permissions

chown -- Change ownership

head -- Display first few lines of a file

touch -- Update access and modification of a file

df -k -- Check disk

du -- Check disk usage

ps -ae | grep mongo

To  count the number of lines or rows in a file, use wc
```
wc -l <filename>
``` 

Find a file recursively in the current directory using grep with regular expressions.  In this example, to ignore upper case or lower case:

    find . -print | grep -i "posts*"




    grep -R searchterm --exclude-dir=DIR --ignore-case
    
Example:

    grep -R signIn --exclude-dir="\.meteor*" --ignore-case


Install on the command line:
    curl -L -O <URL of file>
    
Example:
    curl -L -O https://download.elastic.co/elasticsearch/release/org/elasticsearch/distribution/tar/elasticsearch/2.1.1/elasticsearch-2.1.1.tar.gz


To get a file using curl rather than using wget:
    curl -O <URL of file>


Where is the program such as logstash installed?
Example:

    whereis logstash
    

To remove Windows hidden characters from a file:
    dos2unix filename

To autocomplete based on previous entries:
    CTRL + r
    Type out command and if you see the command you want then press enter.


More find commands:

find . -type f -exec grep <keyword> {} \; -print

find / -type d -name "hadoop_env*"


tar:

http://www.howtogeek.com/248780/how-to-compress-and-extract-files-using-the-tar-command-on-linux/


Recursively find all symbolic links in a directory tree

```
ls -lR /path/to/directory | grep ^l
```

File Editing
===========
To write a new file that has all occurrences of a text beginning with ".example" on a line. Remember to escape the "."

grep "/^\s*\.example" filename > newFilename

sed 's/old/new' myfile

awk


REFERENCES
==========
http://www.thegeekstuff.com/2012/07/wget-curl/

