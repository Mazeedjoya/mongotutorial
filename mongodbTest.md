1. Create a collection named "books" in MongoDB.
```
 db.createCollection("books")
```
2. Insert a document into the "books" collection with the following details:

  Title: "The Great Gatsby"
  Author: "F. Scott Fitzgerald"
  Year: 1925
 ``` 
 db.books.insertOne({Title: "The Great Gatsby",
                    Author: "F. Scott Fitzgerald",
                    Year : 1925
                    })
```
3. Insert another document into the "books" collection with the following details:

  Title: "To Kill a Mockingbird"
  Author: "Harper Lee"
  Year: 1960
```
  db.books.insertOne({
    Title : "To Kill a Mockingbird",
    Author: "Harper Lee" ,
    Year : 1960
  })
```
4. Write a query to find all documents in the "books" collection.
```
db.books.find()
```
5. Write a query to find documents in the "books" collection where the author is "F. Scott Fitzgerald".
```
db.books.find({Author:"F. Scott Fitzgerald"})
```
6. Write a query to find documents in the "books" collection where the year is greater than 1950.
```
db.books.find({Year :{$gt :1950}})
```
7. Write an update query to change the author of the document with the title "To Kill a Mockingbird" to "Harper Lee (edited)".
```
db.books.updateOne({Title: "To Kill a Mockingbird"},{$set:{Title :"Harper Lee"}})
```
8. Write an update query to add a new field "genre" with the value "Fiction" to all documents in the "books" collection.
```
db.books.updateMany( {}, {$set:{genre: "Fiction"}})
```
9. Write a query to find documents in the "books" collection where the genre is "Fiction".
```
db.books.find({genre:"Fiction"})
```
10. Write a query to find documents in the "books" collection where the title starts with the letter "T".
```
db.books.find({title: /^T/})
```
11. Write an update query to increment the year by 1 for all documents in the "books" collection.
```
db.books.updateMany({} ,{$inc:{Year:1}})
```
12. Write a query to find documents in the "books" collection where the year is between 1950 and 1970.
```
db.books.find({Year: {$gte:1950 , $lte:1970}})
```
13. Write a query to find documents in the "books" collection where the author's name contains the letter "a".
```
db.books.find({Author: /a/})
```
14. Write an update query to remove the "genre" field from all documents in the "books" collection.
```
db.books.updateMany({}, {$unset:{genre:""}})
```
15. Write a query to find documents in the "books" collection where the author's name ends with the letter "y".
```
db.books.find({Author: /y$/})
```
16. Write an update query to change the title of the document with the author "Harper Lee" to "Go Set a Watchman".
```
db.books.updateOne({Title : "Harper Lee"}, {$set:{Title: "Go Set a Watchman"}})
```
17. Write a query to find documents in the "books" collection where the title contains the word "Great".
```
db.books.find({Title: /Great/})
```

18. Write a query to find documents in the "books" collection where the title is an exact match for "The Great Gatsby".
```
db.books.find({Title : "The Great Gatsby"})
```
19. Write an update query to add an array field named "categories" with the values ["Classic", "Fiction"] to all documents in the "books" collection.
```
db.books.updateMany({}, {$set: {categories:["Classic" , "Fiction"]}})
```
20. Write a query to find documents in the "books" collection where the "categories" field contains the value "Fiction".
```
db.books.find({categories:"Fiction"})
```
21. Write a query to find documents in the "books" collection where the title contains the word "The" in a case-insensitive manner.
```
db.books.find({Title: /The/})
```
22. Write a query to find documents in the "books" collection where the author's name starts with the letter "J".
```
db.books.find({Author: /^J/})
```
23. Write an update query to increment the "year" field by 5 for all documents in the "books" collection.
```
db.books.updateMany({}, {$inc :{Year:5}})
```
24. Write a query to find documents in the "books" collection where the title is not equal to "Moby Dick".
```
```

25. Write a query to find documents in the "books" collection where the author's name is either "J.K. Rowling" or "George R.R. Martin".
```
db.books.find({$or:[{Author:"J.K.Rowling"}, {Author: "George R.R. Martin"}]})
```
26. Write a query to find documents in the "books" collection where the year is either 2000 or 2010.
```
db.books.find({$or:[{Year: 2000} , {Year: 1966}]})
```
27. Write an update query to multiply the "year" field by 2 for all documents in the "books" collection.
```
```

28. Write a query to find documents in the "books" collection where the title ends with the letter "s".
```
db.books.find({Title: /s$/})
```
29. Write a query to find documents in the "books" collection where the author's name is not in ["Stephen King", "Agatha Christie"].
```
db.books.find({Author:{$nin:["Stephen King" , "Agatha Christie"]}})
```
30. Write an update query to set the "year" field to 2022 for the document with the highest year in the "books" collection.
```
```
