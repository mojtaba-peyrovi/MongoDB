### MONGODB BASICS:

---

Resource: [ProgrammingKnowledge Youtube channel](https://www.youtube.com/watch?v=GtD93tVZDX4&list=PLS1QulWo1RIZtR6bncmSaH8fB81oRl6MP)

__Differences between SQL and noSQL (relational and non-relational databases):__
```
MongoDB: collections ===> SQL: tables
MongoDB: Documents ===> SQL: rows
MongoDB: Fields ===> SQL: columns
```
Collections are not strict about what is inside or we can say they are schema-less.

After we install MongoDB, we can find the executables here:
```
C:\Program Files\MongoDB\Server\4.0\bin
```
and we need to use two of them:
```
mongo.exe   // command line shell
mongod.exe  // mongo deamon that does the background connections
```
anytime we want to work with mongodb, we need to run `mongod.exe` first to make the connection, then we run `mongo.exe` and run the shell.

In order to run `mongod.exe` we open the terminal inside the `bin` folder, and the run mongod.exe. But in order for it to work, we need to have a data structure like this:
```
c:\data\db
```
we need to create it first. after creating it, we can run mongod.exe in a terminal and in another terminal, we run mongo.exe and we are all set.


#### Studio 3T: 

It's a GUI for MongoDB, used to be called MongoChef. I added mongo bin folder to environmental variables, and made it global. Then installed the GUI and connected to the GUI. All ready to use.

Anytime we want to run the GUI, we need to run `mongod` in the terminal and let it connect.

#### Creating Databases:
For making a database all we have to do is saying:
```
use <db_name>  e.g.  use my_db  
```
It looks if there is any database with this name, it uses it, otherwise it creates the database and uses it.

In order to see which database is being used:
```
db
```
running the above command tells us what is the current database.

In order to see all databases available:
```
show dbs
```
It shows all databases. `If the database is empty, it won't be shown in the list.`

#####The hierarchy of objects in a Mongodb database:
```
Database->Collections->Documents
```
In order to add documents into the database we need to say:
```
db.my_collection.insert( {"key1":"value1","key2":value2 } )
```
__NOTE:__ The above db means the database in use. and We made a collection right away and named it my_collection. Then inside insert() we add json value-pairs. (If the value is not string don't put double quote for it.)

Example:
```
db.my_collection.insert({"name":"Moji","age":37, "wealth":"Millionaire"})
```
Now if we run `show dbs` we will see the name of the database we recently created.

#### Dropping a Database:
In order to drop a database, we just have to say:
```
db.dropDatabase()
```
It will drop the current database.

#### Creating a Collection:

We say:
```
db.createCollection("name")  e.g.  db.createCollection("my_collection")
```

#### Dropping a Collection:
```
db.my_collection.drop()
```
