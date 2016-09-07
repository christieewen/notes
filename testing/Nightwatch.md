

On Windows
----------
```sh
   node nightwatch.js -c nightwatch.json --env default
```

Make sure your selenium driver is in the path searchable by your configuration file (nightwatch.json)

On Windows at the bare minimum
-------------------------------
Run Selenium manually
```sh
   java -jar ./node_modules/selenium-server-standalone-jar/jar/selenium-server-standalone-2.45.0.jar
```

Edit the nightwatch.json file to not start selenium since you're starting it manually
```sh
 "selenium": {
    "start_process": false,
    }
```

Run node nightwatch.js -c nightwatch.json --env default
