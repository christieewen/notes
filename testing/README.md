TESTING and Q/A Engineering
===========================

Circle
------
Wait for a command to complete

```sh
while true; do if nc -zw1 localhost 3000; then break; fi; sleep 5; done
```


Nightwatch.js
-------------

    before and after hooks

    data driven tests

https://www.youtube.com/watch?v=794uaoenv_M


         ___Nightwatch.js
        |___data
        |   |_____dev.js
        |   |______staging.js
        |___tests
            |____login.js





REFERENCES

https://github.com/circleci/circleci-docs/blob/master/jekyll/_docs/background-process.md

http://unix.stackexchange.com/questions/190513/shell-scripting-proper-way-to-check-for-internet-connectivity

https://github.com/circleci/circleci-docs/blob/master/jekyll/_docs/background-process.md
