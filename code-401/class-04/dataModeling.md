# Data Modeling

## NoSQL vs SQL

1. What type of database is the best fit for the complex query intensive environment?

    SQL databases are a good fit for the complex query intensive environment. This is because SQL databases use SQL (strctured query language) for defining and manipulating data, which is very powerful. On a high level, NoSQL databases don't have standard interfaces to perform complex queries, and the queries themselves in NoSQL   are not as powerful as the SQL query language. 

2. What type of database is the best fit for hierarchical data storage?

    NoSQL databases are a better fit for hierarchical data storage. They follow the key-value pair way of storing data similar to JSON data. SQL databases are not the best fir for hierarchical data storage. 


3. Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.

    Imagine you have a single tall building (SQL database) and you want to accomodate more people. One way to do that is to add more floors to that building, making it taller. This is called vertical scaling. On the other hand, imagine you have a lot of smaller houses (NoSQL database) spread out in a neighborhood. If you want to accommodate more people, you can simply build more houses in the available spaces. This is called horizontal scaling. In simpler terms, SQL databases grow by making the existing structure bigger (vertically scalable), while NoSQL databases grow by adding more structures (horizontally scalable). 