**1 : What is MongoDB**

MongoDB is a document database and can be installed locally or
hosted in the cloud.

**2: How can we use mongoDB in shell or UI?**

you have to install mongo db in shell via Step 

1- update wsl to v 2
https://gist.github.com/djfdyuruiry/6720faa3f9fc59bfdf6284ee1f41f950
https://winaero.com/update-from-wsl-to-wsl-2-in-windows-10/
2- install mongodb in ubuntu
wget -qO - https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" |
sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list
sudo apt-get update
sudo apt-get install -y mongodb-org
3- connect your mongo with shell
mongo "mongodb+srv://cluster0.lqwfl.mongodb.net/myFirstDatabase" --username user

**3: How To create database, table and insert data in mongoDB?**

Method 1
You can create a collection using the createCollection() database method.
Example
db.createCollection("posts")
Method 2
You can also create a collection during the insert process.
Example
We are here assuming object is a valid JavaScript object containing post data:
db.posts.insertOne(object

insertOne()
To insert a single document, use the insertOne() method.
This method inserts a single object into the database.
Note: When typing in the shell, after opening an object with curly braces


**4: How to order by in mongoDB?**

Find Data
There are 2 methods to find and select data from a MongoDB collection, find() and findOne().
find()
To select data from a collection in MongoDB, we can use the find() method.
This method accepts a query object. If left empty, all documents will be returned.
Example
db.posts.find()
db.posts.findOne()

**5: How to update data in mongoDB?**

Update Document
To update an existing document we can use the updateOne() or updateMany() methods.
The first parameter is a query object to define which document or documents should be updated.
The second parameter is an object defining the updated data.
updateOne()
The updateOne() method will update the first document that is found matching the provided query.
Let's see what the "like" count for the post with the title of "Post Title 1":
Example
db.posts.find( { title: "Post Title 1" } )
updateMany()
The updateMany() method will update all documents that match the provided query.
Example
Update likes on all documents by 1. For this we will use the $inc (increment) operator:
db.posts.updateMany({}, { $inc: { likes: 1 } })


**6: How to delete data in mongoDB?**

deleteOne()
The deleteOne() method will delete the first document that matches the query provided.
Example
db.posts.deleteOne({ title: "Post Title 5" })
Try it Yourself »
deleteMany()
The deleteMany() method will delete all documents that match the query provided.
Example
db.posts.deleteMany({ category: "Technology" })


**7: How to select data in mongoDB?**

findOne()
To select only one document, we can use the findOne() method.
This method accepts a query object. If left empty, it will return the first document it finds.
Note: This method only returns the first match it finds.
Example
db.posts.findOne()

or 

db.posts.find()
