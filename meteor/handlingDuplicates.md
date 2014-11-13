To avoid duplicates in Meteor, use Collections._ensureIndex( { a: 1 , b: 1}, { unique: true, dropDups:true} )

You can define your index on the server side code in the meteor startup code or where the collection is defined.

See http://docs.mongodb.org/manual/reference/method/db.collection.ensureIndex/

