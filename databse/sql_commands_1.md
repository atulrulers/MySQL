#### to connect to database using cmd/terminal
$ mysql -u <username> -p

#### to show all the database
$ show databases;

#### to create database
$ create database greg_list;

#### to use database
$ use greg_list;

#### to show all the tables in database
$ show tables;

#### to create tables
$ CREATE TABLE my_contacts (
		last_name VARCHAR(30),
		first_name VARCHAR(30),
		email VARCHAR(50),
		birthday DATE,
		gender CHAR(1),
		profession VARCHAR(50),
		location VARCHAR(50),
		status VARCHAR(20),
		interests VARCHAR(100),
		seeking VARCHAR(100)
	);

#### to describe the table
$ DESC my_contacts;

#### drop table -- deletes table and any data init
$ DROP TABLE my_contacts;


#### To add data to your table

$ INSERT INTO my_contacts
		(last_name, first_name, email, gender, birthday,
		profession, location, status, interests, seeking)
		VALUES
		('Anderson', 'Jillian', 'jill_anderson@breakneckpizza.net', 'F', '1980-09-05', 'Technical Writer', 'Palo Alto, CA', 'Single', 'Kakaking, Reptiles', 'Relationship, Friends');



$ INSERT INTO my_contacts (
	first_name , email, profession, location
) VALUES (
	'pat' , 'patpost@break.ent', 'Postal Worker', 'Princeton, NJ '
);


#### desc only show the structures of table, not the data
#### to get the data from table use SELECT

$ SELECT * FROM my_contacts;







