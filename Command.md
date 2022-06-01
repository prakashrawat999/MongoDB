# Mongo DB Commands

## Start Shell
```bash
mongo
mongo.exe
```
## Show All Databases
```bash
show dbs
```
## Create New Database & Switch Database (same query)
```bash
use database_name
```
## Know Your Current Database
```bash
db database_name
```
## Drop Database
1. step : select database using (use database_name) 
2. step : db. dropDatase()
```bash
db.dropDatabase()
```
## Create Collection (Table)
```bash
db.createCollection(name)
```

## Show Collection
```bash
show collections
```
##  Drop Collection
```bash
db.collection_name.drop()
```
return true if drop else false

## Insert Document in Collection (Insert row in table)
```bash
db.collection_name.insert({"_id ": 101, "name":"prakash"})
```
* If you want to give id than you can  use (_id) else automatically assign.
```bash
db.collection_name.insertOne({"name":"rawat"})
```
* If you want to insert single data.
```bash
db.collection_name.insertMany([
    {"name":"prakash"},
    {"name":"pankaj"},
    {"name":"piyush"},
    {"name":"arvind"}
    ])
```
* If you want to insert multiple data.

## Show Collection Documents ( Display table rows)
```bash
db.collection_name.find()
db.collection_name.find().pretty()
```
## Count Documents
```bash
db.posts.find().count()
db.posts.find({ 'age': 19 }).count()
```
## Sort Documents
```bash
# Ascending Order using 1
db.posts.find().sort({ age : 1 }).pretty()
# Descending Order using -1
db.posts.find().sort({ age : -1 }).pretty()
```
## Limit & Chaining
```bash
db.posts.find().limit(2).pretty()
db.posts.find().limit(2).sort({ age : 19 }).pretty()
```
## Update Document
```bash
db.collection_name.update(selection_criteria, update_data)
db.rawat.update({'name':'golu'},{$set:{'name':'prakash'}})
```
Return { matched: 1, modified: 1 }

```bash
db.collection_name.updateOne({'_id':3},{$set:{'age':20}})
db.rawat.updateOne({"name":"prakash rawat"},{$set:{"roll":0345}})
```
Return { "acknowledged" : true, "matchedCount" : 1, "modifiedCount" : 1 }

```bash
db.collection_name.updateMany({"age":19},{$set:{"eligible":true}})
```
Return { "acknowledged" : true, "matchedCount" : 1, "modifiedCount" : 1 }
## Delete/Remove Document
```bash

```


