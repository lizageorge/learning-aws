# Form Over Data applications and Databases
> April 7, 2019 
> From Acha :yellow_heart: , showing Quickbooks code and sleepTracker Excels as examples. 
## Form over Data
* = A type of application, where you can have a **form**, which is a list of columns of values that can be *entered or derived* (calculated from the values entered), and that data will be stored to be retrieved later. 
* [#sleepTracker] you can have columns called ‘bedTime’ and ‘wakeUpTime’ which the user will enter, and ‘sleepTime’ which the app will derive with a function that uses bedTime and wakeUpTime. The app is made to give an interface for users to enter bedTime and wakeUpTime and receive sleepTime
* You can think of it *like an excel*, with some columns of entered values and some columns of derived values

## Databases
* = a way of storing values so that it’s easy to retrieve easily, and so that data isn’t repeatedly stored. 
* It can consist of **tables** (what excel would call a Sheet), each table will have columns (excel calls it A, B C… but here the columns can be named) and each column would have a value. Each row would have a **‘id’ value**, so the first column is technically called ‘id’
* [] quickbooks is the database, with a list of tables (user, address), each table has a list of fields (‘address’ might have ‘city’, ‘state’, ‘zipcode’)
* **Linking** - you can link an entry in one table to another table. [#sleepTracker] a table called sleepTracker containing all of the bedTimes and wakeUpTimes of all users doesn’t have to also include every user’s FirstName and lastName. A separate table called ‘users’ can have a unique id in front of every entry, and each entry in the sleepTracker table can just include that unique id. 
* Can retrieve values using **SQL (Structured Query Language)**, including the values from linked tables
```
|||| select * from user; |||||     \ 1  John  Doe   2
                                    2 Jane  Doe 	2
```

* The ‘*’ means ‘every field’ but you can specify the field, like ‘firstName’
* You can use the functions of SQL like ‘where’ and ‘group by’ to filter or sort out the retrieved values
```
||||select * FROM user where lastName = ‘Doe’ ; ||| \\\ [just the Doe family’s info]
```
