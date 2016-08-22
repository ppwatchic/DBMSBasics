####Schema
###Schema
##Schema

Schema is a word used in database domain. It is closely to the concept ofstructure in C, or fields in Java. 
It will be too lenghy for me to describe what it exactly is.  

In C language, If we define a StudentProfile structure, it looks like this: 
```
struct StudentProfile {
   string  firstName;
   string lastName;
   string  studentID;
   boolean  gender;
   string   major;
} ; 
```

In Java, we will define a class StudentProfile.java, it looks like this: 
```
public class StudentProfile {
  // the fields 
  private String firstName;
  private String lastName;
  private final String studentID;
  private boolean gender;
  private String major;
  // omit methods here 
}
```

And in DataBase (SQL flavor), if we define a database called student, and a table called StudentProfile. We can describe the table in this way: 
```
CREATE TABLE StudentProfile(
  firstName varchar(32) NOT NULL,
  lastName varchar(32) NOT NULL,
  studentID varchar(20),
  gender BOOL,
  major varchar(32),
),
```

And in other NoSQL database language, for example in ElasticSearch, It will look like this: 
```
"studentProfile": {
            "properties": {
               "firstName": {
                  "type": "string"
               },
               "lastName": {
                  "type": "string"
               },
               "studentID": {
                  "type": "string"
               },
               "gender": {
                  "type": "boolean"
               },
               "major": {
                  "type": "string"
               }
            }
          }
```

| C | Java | SQL | ElasticSearch |
| --- | --- | --- | --- |
| structure | fields | schema | mapping; or schema definition |

