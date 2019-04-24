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


