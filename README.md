# column-family-database

Cassandra is a free and open-source, distributed, wide-column store, NoSQL database management system designed to handle large amounts of data across many commodity servers, providing high availability with no single point of failure.

First, let's create a keyspace (database) for our online shopping platform:

              CREATE KEYSPACE shopping_platform WITH replication = {'class': 'SimpleStrategy', 'replication_factor': 1};
             
Now, to perform insert, delete, update, and search operations for customer data analysis, we can use the following examples:
                
Syntax for creating table
-------------------------
Now, let's create a table for customer data:

                CREATE TABLE customers (
                customer_id uuid,
                name text,
                email text,
                phone_number text,
                address text,
                PRIMARY KEY (customer_id)
                );
                
                cqlsh:shopping>CREATE TABLE products (
                product p_id,
                product_name TEXT,
                product_price decimal,
                PRIMARY KEY(p_id)
                );


Insert Operation
----------------
To insert a new customer:

         INSERT INTO customers (customer_id, name, email, address, phone_number, registration_date) VALUES ('1', 'John Doe', 'john.doe@example.com', '123 Main St',              '555-555-55');
         
         cqlsh:shopping>INSERT INTO products (product,name,prize) VALUES (11,'laptop','125000');

Delete Operation
-----------------
To delete a customer:

           DELETE FROM customers WHERE customer_id = '1';

Update Operation
-----------------
To update a customer's phone number:

          UPDATE customers SET phone_number = '555-555-1234' WHERE customer_id = '1';

Search Operation
----------------
To search for all orders placed by a customer:

          SELECT * FROM orders WHERE customer_id = '1';
          
Conclusion
----------
            This readme file explain about how to create tables using cassendra query language and perform opreations like insert,delete,update and search.
