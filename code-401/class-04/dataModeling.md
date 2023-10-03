# Data Modeling

## NoSQL vs SQL

1. What type of database is the best fit for the complex query intensive environment?

    SQL databases are a good fit for the complex query intensive environment. This is because SQL databases use SQL (strctured query language) for defining and manipulating data, which is very powerful. On a high level, NoSQL databases don't have standard interfaces to perform complex queries, and the queries themselves in NoSQL   are not as powerful as the SQL query language. 

2. What type of database is the best fit for hierarchical data storage?

    NoSQL databases are a better fit for hierarchical data storage. They follow the key-value pair way of storing data similar to JSON data. SQL databases are not the best fir for hierarchical data storage. 


3. Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.

    Imagine you have a single tall building (SQL database) and you want to accomodate more people. One way to do that is to add more floors to that building, making it taller. This is called vertical scaling. On the other hand, imagine you have a lot of smaller houses (NoSQL database) spread out in a neighborhood. If you want to accommodate more people, you can simply build more houses in the available spaces. This is called horizontal scaling. In simpler terms, SQL databases grow by making the existing structure bigger (vertically scalable), while NoSQL databases grow by adding more structures (horizontally scalable). 

    ## SQL Modeling Techniques
    
    1. Among data tables, what is a one-to-many relationship and how do we “relate” them?

        A one-to-many relationship in data tables means that an entry in one table can be related to more than one entry in another table. For instance, let's say we have a scenerio where many employees are in one department. This relationship is depicted as a one-to-many relationship. The relationship between tables is established using foreign keys. The match between a foreign key and the primary key in another table is what "glues" the database together. This relationship becomes particularly significant when joining tables together. 

    2. Prior to designing your relational database, it might be useful to __a__ of the database tables and their relationships. 

        Priior to designing your relational database, it might be useful to create diagrams of the database tables and their relationships. These diagrams can help visualize the structure of the database and the interdependencies between tables. 

    3. Explain the difference betweena primary and foreign key. 

        - A *primary key* uniquely identifies each row in a table. A table typically has one primary key, but it can have more. When the key comprises more than one column, it's called a compound key. 
        
        - A *foreign key* is a column or set of columns in a table that matches a primary key in another table. The match between foreign key and the primary key is what connects or "relates" tables in a relational database. The significance of these relationships becomes evident when we start to work on joining tables together. 