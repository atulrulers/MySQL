#### MORE ON SELECT STATEMENT

$ INSERT INTO my_contacts (
	last_name, first_name,
	email, gender, location
	) 
	VALUES (
	'Jacobs', 'Anne',
	'anne123@programmersboat.com',
	'F', 'San Jose, CA'
	) ;

#### select * -- will return all the column from database
#### select * without where condition will return all the 
#### from the table

#### WHERE -- statement in select

$ SELECT * FROM my_contacts WHERE first_name = 'Anne';

#### practice

$ CREATE TABLE easy_drinks (
	drink_name VARCHAR(20) NOT NULL,
	main VARCHAR(15) NOT NULL,
	amount1 DEC(4,2) NOT NULL DEFAULT 1,
	second VARCHAR(20),
	amount2 DEC(4,2),
	direction VARCHAR(100)
	);

#### inserting data
#### to insert into all the row specified during creation of table , remember order should be maintained
$ INSERT INTO easy_drinks VALUES 
	(
		'Blackthron', 'tonicwater', 6.5, 'apple juice', 1,
		'stir with ice, strain into cocktail glass with lemon twist'
	);

#### some selects statements
$ SELECT * FROM easy_drinks WHERE amount1 < '1.5' ;

#### select only specified columns
$ SELECT drink_name , main, amount1 from easy_drinks;

#### select only specified columns for only specific row

$ SELECT drink_name , main, amount1 from easy_drinks WHERE main = 'soda';

#### AND clause

$ SELECT drink_name , main, amount1 from easy_drinks WHERE main = 'soda' AND amount1= 1.5;

#### COMPARISION > , < , >= , <= , = , <>, is null

$ SELECT * FROM my_contacts WHERE interests IS NULL ; 

#### KEYWORD :- **LIKE**

SELECT * FROM my_contacts WHERE location LIKE '%ca' ;

#### Like teams up with wildcards characters. 
#### wild cards are stand-ins for the characters that are atually there. Rather like a joker in a card games, a wildcards is equal to any character in a string

#### % -- stand-in for any number of unknown character

#### _ -- stand-in for one unknown character

#### search between the range

$ SELECT * FROM easy_drinks WHERE amount1 >= 1.0 and amount1 <= 1.5 

#### use BETWEEN keyword instead --> it will return the same result as previous queries

$ SELECT * FROM easy_drinks WHERE amount1 BETWEEN 1.0 AND 1.5 ;

#### BETWEEN -- this keyword means [] not () this


#### IN keywords -- matches the where clause with multiple value and it can be used in place for multile OR 

$ SELECT first_name FROM my_contacts WHERE location = 'san jose, ca' or location = 'boston, ma' or location = 'Neyork, NY' ;

#### above statement can be solved by using IN operator which is much cleaner

$ SELECT first_name FROM my_contacts WHERE location IN ('san jose, ca', 'boston, ma', 'newyork ny');

#### and location NOT IN
$ SELECT first_name FROM my_contacts WHERE location NOT IN ('san jose, ca', 'boston, ma', 'newyork ny');

#### NOT has multiple use
#### NOT goes right after WHERE clause
