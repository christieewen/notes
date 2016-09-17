Date
====
"Note: parsing of date strings with the Date constructor (and Date.parse, they are equivalent) is strongly discouraged due to browser differences and inconsistencies." - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date

http://www.bennadel.com/blog/3115-maintaining-javascript-date-values-during-deserialization-with-a-json-reviver.htm

In a nutshell, return new Date(value).
http://stackoverflow.com/questions/1792865/how-to-use-json-parse-reviver-parameter-to-parse-date-string
