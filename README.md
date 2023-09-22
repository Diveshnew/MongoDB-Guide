# MongoDB CRUD Operations Reference

This repository provides a comprehensive guide to perform CRUD (Create, Read, Update, Delete) operations in MongoDB. Whether you're new to MongoDB or need a quick reference, this README will assist you in understanding and executing these fundamental database operations.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
3. [MongoDB Basics](#mongodb-basics)
   - [1. Create](#1-create)
   - [2. Read](#2-read)
   - [3. Update](#3-update)
   - [4. Delete](#4-delete)
4. [Examples](#examples)


## Prerequisites

Before you begin, make sure you have the following prerequisites installed:

- MongoDB: Download and install MongoDB from [https://www.mongodb.com/try/download/community](https://www.mongodb.com/try/download/community).
- Start it by Using this command and You should be at the ~ directory.
```
mongod
```
- After that open another Tab and use this command to run it>
```
mongosh
```

## Installation

Clone this repository to your local machine using the following command:

```bash
git clone https://github.com/diveshnew/MongoDB-Guide
```

## MongoDB Basics

## 1. Create
To insert data into a MongoDB collection, you can use the `insertOne` or `insertMany` methods. Here's an example:

```
// Insert a single document
db.collection('your-collection').insertOne({ key: 'value' });

// Insert multiple documents
db.collection('your-collection').insertMany([
  { key1: 'value1' },
  { key2: 'value2' },
]);
```
- Additional Commands
```
// For taking a look at all the databases
Show dbs

// For using and making the new database here it is shopDB
use shopDB

// Watching the current active database
db

// for listing all the current collections or tables in the current db
show collections
```

## 2. Read
To retrieve data from a MongoDB collection, you can use the find method. Here's an example:

```
// Find all documents in a collection
const allDocuments = db.collection('your-collection').find();

// Find documents with a specific condition
const filteredDocuments = db.collection('your-collection').find({ key: 'value' });
```

## 3. Update
To update documents in a MongoDB collection, you can use the `updateOne` or `updateMany` methods. Here's an example:
```
// Update a single document
db.collection('your-collection').updateOne({ key: 'value' }, { $set: { newKey: 'newValue' } });

// Update multiple documents
db.collection('your-collection').updateMany({ key: 'value' }, { $set: { newKey: 'newValue' } });
```

## 4. Delete
To remove documents from a MongoDB collection, you can use the `deleteOne` or `deleteMany` methods. Here's an example:
```
// Delete a single document
db.collection('your-collection').deleteOne({ key: 'value' });

// Delete multiple documents
db.collection('your-collection').deleteMany({ key: 'value' });
```
