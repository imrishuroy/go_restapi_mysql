1. Create a mysql docker container

    docker run --detach --env MYSQL_ROOT_PASSWORD=dummypassword --env MYSQL_USER=imrishuroy --env MYSQL_PASSWORD=123456 --env MYSQL_DATABASE=product_database --name mysql --publish 3306:3306 mysql:8-oracle

2. Open mysql shell and connect 

    \connect imrishuroy@localhost:3306

3. switch to SQL mode

    \sql

4. select the database 

    use product_database;

5. Create a product table
   
    CREATE TABLE `product` (
    `code` varchar(20) NOT NULL DEFAULT 'x',
    `name` varchar(150) DEFAULT NULL,
    `qty` int(5) DEFAULT NULL,
    `last_updated` datetime DEFAULT NULL
    ) ENGINE=InnoDB DEFAULT CHARSET=utf8;

6. Check whether the table is created or not

    show tables;

7. check entries in the table

    select * from product;       
