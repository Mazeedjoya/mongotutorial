

# DATABASE
```
use wecodeacademy 
```
# Student
```
db.createCollection("student") 
	id
	name
	fathername
	address
	mobile
	email
	admissiondate 
	dob
```


# BATCH 
```
  db.createCollection("batch")
  
	id 
	coursename
	startdate
	enddate
```

1. Vo sare students ki list btao jinka email ni hai 
```
db.student.find({email:{$exists:false}})
```
2. Vo sare students ki list btao jinka mobile number same hai 
```
```

3. Sare students ka only email and mobile return krvao
```
db.student.find({},{email:1, mobile:1}) 
```

4. students record ki name se sorting krni hai 
```
db.student.find().sort({name:1}) 
```

5. vo sare students ki list return kro jinka admission last 3 months me hua hai 
```
```
6. vo sare students ka only naam btao jinka admission current month me hua hai 
```
```
7. vo sare students ka naam btao jinki dob year same hai 
```
```
8. vo sare students ka naam btao jinka address jaipur, nagaur ya karauli ho 
```
db.student.find({ address: { $in: ["Jhhotwara", "aman street Jhhotwara"] } }) 
```

9. vo sare students ka naam btao jo Sikar, Jhunjhun se ni hai 
```
```

10. vo sare students ka naam btao jinka Address Sikar hai and fathername Rahim hai 
```
 db.student.find({$and:[{"address":"sikar"},{"fathername":"Rahim"}]}) 
```

11. vo sare students ka naam btao jinka fathername Khalil ho or email id rahim@gmail.com ho 
```
db.student.find({$and:[{"email":"rahim@gmail.com"} ,{"fathername":"Khalil"}]}) 
```

12. question 11 ko nor se kro 
```
db.student.find({$nor:[{"email":"rahim@gmail.com"} ,{"fathername":"Khalil"}]}) 
```

13. Vo sare students ka naam btao jinka father name Ahmed ni hai 
```
db.student.find({fathername:{$ne:"Ahmed"}}) 
```

14. Vo sare students ka naam btao jinka mobile 945345435 ni hai
 ```
  db.student.find({"mobile":{$not:{$eq:945345435}}})
 ```
