Page Objects
------------
/tests/nightwatch/pages/pageObject.js
```sh
   module.exports = {
      url: 'https://localhost:3000',
      commands: [{
         "completePageUsingLoop": function(userData){
      var client = this; // the value of this changes inside of the forEach section below so we're storing 'this' in client
      
      client
        .waitForElementPresent('#page_2', 3000)

        .click("input[name='2_0'][value='" + userData.someValue + "']")

      var elemArray = ["elemA", "elemB", "elemC", "elemD", "elemE"];
      if (Array.isArray(userData.elements)) {
        (userData.elements).forEach(function(oneElement) {
          client
            .click("input[id='2_1_" + elemArray.indexOf(oneElement) + "'][value='" + oneElement + "']")
        });
      } else {
          client
            .click("input[id='2_1_" + elemArray.indexOf(userData.elements) + "'][value='" + userData.elements + "']")
      }

      client
        .waitForElementPresent('#page_2Next', 3000)
        .click("#page_2Next")
        .waitForElementPresent('#page_3', 3000);
      return client;
      }
      }]
```

/private/data/userData.js
```sh
module.exports = [{
  "email": "example@example.com",
  "password": "password",
  "verificationCode": "abc",
  "id": "123",
  "data": {
    "birthdate": "12-31-1999",
    "someOtherData": "something other"
  }
},{
  "email": "example2@example2.com",
  "password": "password",
  "verificationCode": "def",
  "id": "345",
  "data": {
    "birthdate": "12-31-1999",
    "someOtherData": "something other"
  }
  }]
```

/tests/nightwatch/globals.js
```sh
module.exports = {
  "default" : {
    "launchUrl": "http://localhost:3000",
    "urls": {
      "login": "http://localhost:3000"
    },
    "users" : require('../../private/data/userData.js'),
}
```


```sh
module.exports = {
  tags: ['tagA', 'tagB'],
  beforeEach: function(client){
    const users = client.globals.users;

    client
      .url("http://localhost:3000").pause(3000)
      .executeAsync(function(data){
        Meteor.call('dropTestUsers');

        data.forEach(function(user){
          Meteor.call('initializeUser', user.email, user.password);
        });
      }, [users]);
  },
  "Page Title": function(client){
    client
      .resizeWindow(1200, 1800)
      .pause(3000)

    const pageObject = client.page.pageObject();

    client.globals.users.forEach(function(user){

      client
        .url("http://localhost:3000")
        .sectionBreak(user.email)

      pageObject
        .login(user.email, user.password, client)
        .completePageUsingLoop(user);

      client
        .executeAsync(function(data){
          Meteor.logout();
        });

    });
  },
  "End": function (client) {
    client
      .end();
  }
};
```


References:
http://nightwatchjs.org/guide#page-objects

http://martinfowler.com/bliki/PageObject.html

http://martinfowler.com/bliki/TellDontAsk.html

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
