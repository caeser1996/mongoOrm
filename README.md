# mongoOrm
## Here is an example of an ORM (Object-Relational Mapping) for MongoDB in Python using the PyMongo library:

# This class provides basic CRUD (Create, Read, Update, Delete) operations for MongoDB by using the PyMongo driver. You can use it as follows:

```
orm = MongoORM("mydb", "mycollection")

# insert one document
orm.insert_one({"name": "John Doe", "age": 30})

# insert multiple documents
orm.insert_many([{"name": "Jane Doe", "age": 25}, {"name": "Bob Smith", "age": 35}])

# find one document
print(orm.find_one({"name": "John Doe"}))

# find multiple documents
for doc in orm.find_many({"age": {"$gt": 30}}):
    print(doc)

# update one document
orm.update_one({"name": "John Doe"}, {"$set": {"age": 35}})

# update multiple documents
orm.update_many({"age": {"$lt": 30}}, {"$inc": {"age": 5}})

# delete one document
orm.delete_one({"name": "Jane Doe"})

# delete multiple documents
orm.delete_many({"age": {"$gt": 40}})
```
