CREATE TABLE menu (
  no int,
  menu text,
  price INT,
  timepreparation text
);

insert into menu
values (1,"Ham cheese",299,"30 min"),
       (2,"Hawaiian",329,"30 min"),
       (3,"Alhoha",329,"35 min"),
       (4,"Angry chicken",339,"25 min"),
       (5,"double cheese",329,"20 min"),
       (6,"Meat",459,"45 min");

CREATE TABLE customers (
  customerid int,
  Firstname text,
  lastname text,
  Orderid int
);

insert into customers
values (1000,"John","Smith",202021),
       (1001,"Sarah","Miller",202033),
       (1002,"Smith","Domino",202044),
       (1003,"John","Bravo",209011),
       (1004,"Heren","Hercy",209834),
       (1005,"Christain","Davinci",218420),
       (1006,"Chris","Potter",305006),
       (1007,"Chalie","Anger",327433);

CREATE TABLE orders (
  orderid int,
  orderdate date,
  menu text,
  quantity int
);

insert into orders
values (202021,2023-12-30,"Ham cheese",1),
       (202033,2023-12-1,"Alhoha",2),
       (202044,2023-12-13,"Hawaiian",2),
       (209011,2023-12-10,"Angry chicken",1),
       (209834,2023-11-17,"Meat",3),
       (218420,2023-11-22,"Alhoha",1),
       (305006,2023-11-29,"Meat",1),
       (327433,2023-12-15,"double cheese",2);

CREATE TABLE delivery (
  Location text,
  orderid int
);

insert into delivery
values ("Bang khen",202021),
       ("Chatuchak",202033),
       ("samyan",202044),
       ("Phayathai",209011),
       ("samyan",209834),
       ("Chatuchak",218420),
       ("Phayathai",305006),
       ("Sathon",327433);
.mode box

-- Terminal show my welcome and data describtion
.print "\n Welcome to my pizza restaurant database! \n \n"

.print "Please scroll down to see my Database and my SQL samples \n\nFirstly, Let's explore the table to discover data record. \nYou will see this data base including 4 tables menu, customers,orders and delivery \n \n"

-- Show all of recorded data by table
.print "Table name : orders"
select * from orders;

.print "\n\n Table name : customers"
select * from customers;

.print "\n\n Table name : menu"
select * from menu;

.print "\n\n Table name : delivery"
select * from delivery;

.print "\n\n [ SQL query sample ] \n\n 1.) Who is the most quantity of pizza ordered ? \n"

select Firstname, lastname, menu, quantity from customers
join orders on customers.orderid = orders.orderid
order by quantity desc
limit 1;

.print "\n\n2.) From question no.1, What is the total pizza cost ? \n"
select Firstname,lastname, menu.menu, quantity, Price, menu.Price*quantity as Total_price
from customers
join orders on customers.orderid = orders.orderid
join menu on menu.menu = orders.menu
where Firstname = "Heren";

.print "\n\n3.) Who ordered pizza from Bang khen ? \n"
select Firstname, lastname 
from (select * from delivery
join customers on customers.orderid = delivery.orderid
where Location = "Bang khen");
