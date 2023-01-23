from pymongo import MongoClient

class MongoORM:
    def __init__(self, db_name, collection_name):
        self.client = MongoClient()
        self.db = self.client[db_name]
        self.collection = self.db[collection_name]

    def insert_one(self, document):
        self.collection.insert_one(document)

    def insert_many(self, documents):
        self.collection.insert_many(documents)

    def find_one(self, query={}):
        return self.collection.find_one(query)

    def find_many(self, query={}):
        return self.collection.find(query)

    def update_one(self, query, update):
        self.collection.update_one(query, update)

    def update_many(self, query, update):
        self.collection.update_many(query, update)

    def delete_one(self, query):
        self.collection.delete_one(query)

    def delete_many(self, query):
        self.collection.delete_many(query)
