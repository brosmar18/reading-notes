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

## SQL vs NoSQL

1. How do we treat keywords and parameters differently in SQL syntax? 

    In SQL, keywords are predefined words used to perform specific operations. They are part of the SQL language itself. For example, `SELECT`, `FROM`, and `WHERE`. These keywords are used to structure a query and tell the database what action to perform. 

    Parameters, on the other hand, are user-defined and represent specific data or criteria that the user wants to work with. For instance, in the query `SELECT name from  users WHERE age = 25`, `name`, and `age` are parameters that specify which data the user is interested in, while `SELECT`, `FROM`, and `WHERE` are keywords. 

2. Define normalization within the context of schemas and data. 

    Normalization is the process of organizing data within a database to reduce redundancy and improve data integrity. In the context of schemas and data, normalization involves distributing data across different tables in a structured manner. This ensures that each piece of data is stored in only one place, which makes the database more efficient and reduces the chances of data anomalies. The goal is to ensure that data is stored logically, relations between data are clear, and there's minimal data duplication.

3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.

    - **One-to-One**: Imagine you have a box of employee ID cards. Each card has a unique ID number and a matching photo of the employee. In this scenario, one ID number corresponds to one photo. This is a one-to-one relationship, where each item (or "entity") in one group matches exactly one item in another group.

    - **One-to-Many**: Think of a mother duck and her ducklings. One mother duck can have multiple ducklings, but each duckling has only one mother. This is a one-to-many relationship, where one entity from one group can be associated with multiple entities from another group, but not the other way around.

    - **Many-to-Many**: Consider a dance class where students can enroll in multiple dance courses, and each course can have multiple students. Here, there's a many-to-many relationship because multiple entities from one group can be associated with multiple entities from another group.