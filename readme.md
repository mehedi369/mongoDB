# My first Mongo Commands
* mongod => used for running mongo deamon or other word use for running mongodb
* mongo => for running the mongo shell.
* help => for showing help in the mongo shell.
* show dbs => for showing the databases.
* use => for using an existing db or create a new db.
* show collections for showing the current database.

# Most Important
# CRUD
* insert => for inserting data to the database. syntax: db.[nameOfdb].insert({key : "value"}).

* find => for diplaying data or finding given key data. syntax : db.[nameOfdb].find() or db.[nameOfdb].find({key: "value"})

* update => is used for updaing the database. syntax: db.[nameOfdb].update({name: "[value]"}, 
  {$set : {[keyToChange] : "[newValue]"}}) and we can also set the new property by using the new $set object
  the syntax is: db.[nameOfdb].update({name: "[value]"}, {$set : {[newKey] : "[newValue]"}})

* remove => is used for removing or deleting elements from database. In order to delete a collection or value 
  the syntax is: db.[nameOfdb].remove({[nameOfdbKEY]:"[nameOfdbVALUE]"})
* remove => We can also remove the number of or limit the number to remove
  or delete.
  db.[nameOfdb].remove({key: "[value]"}).limit["HowMuchCollectionToDelete"].
