Inspiration
-----------
I was trying to understand how to properly configure nightwatch and starrynight for creating a data driven test environment.

==============================================

Modified version of slides 51, 52, 53 from http://www.slideshare.net/sethmcl/join-the-darkside-nightwatchjs 

Nightwatch.json
---------------
test_settings: {
  default:{
    globals: require('./data/dev')
  }
}

data/dev.js
-----------
module.exports = {
  username: 'seth',
  password: 'html5dev',
  urls: {
    login: 'http://localhost:8000'
  }
};

login.js
--------
module.exports = {
  var data = client.globals;
};


Questions
---------
Why is it ./data/dev and not ./data/dev.js?  Apparently, Node's require will work with both
JSON and JS files.  Not specifiying the extension JS allows for changing the file extensions at anytime without having to
change the calling code.  Read more [here](http://www.bennadel.com/blog/2908-you-can-use-require-to-load-json-javascript-object-notation-files-in-node-js.htm)

It's worthwile to understand the nuances of [require, export and modules in node](http://openmymind.net/2012/2/3/Node-Require-and-Exports/).

What is the preferred setup? Editing the globals.json defined in the globals_path in Nightwatch.json OR globals variable
defined in the test_settings.default
