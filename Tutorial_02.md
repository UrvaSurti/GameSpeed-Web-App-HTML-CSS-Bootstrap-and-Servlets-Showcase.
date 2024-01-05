<a name="br1"></a> 

Tutorial #2

MySQL Datastore

CSP 584 – Enterprise Web Application

Dr. Atef Bader

Illinois Institute of Technology

TA : Prakhar Nag

pnag@hawk.iit.edu



<a name="br2"></a> 

**The Architecture - MVC**

**Database**

7

Product Reviews

1

2

3

6

Database

Servers

Internet

4

App Server

Client

**Database**

5

**Table 2**

**Customer**

**Orders**

**Table 1**

**Registration**



<a name="br3"></a> 

**Pre-Requisites**:

• Install Java latest version into your system.

• Set the PAT H system variable in your local system under

Control Panel –> system-> Advanced system

settings -> Click on Advanced Tab ->Environment variables.

Example PAT H

variable



<a name="br4"></a> 

Platforms supported in MySQL



<a name="br5"></a> 

**Download and Install MySQL Server**

• Download the MySQL installer f rom

https://dev.mysql.c om/downl oads/inst al ler/

• (Choose the my-installer-web- community f ile)

Select this file to

Download and run it.



<a name="br6"></a> 

Select "Custom” as

the setup type and

click Next.



<a name="br7"></a> 

Select the products

to be installed and

click Next.



<a name="br8"></a> 

If you get a “Try

Again “ option here

instead, then click

on the try again

option to download

the products.



<a name="br9"></a> 

Once all the

products are

installed and

the status is

shown as

“complete”

proceed with

the n ext option



<a name="br10"></a> 

Port to

connect to

MYSQL

.



<a name="br11"></a> 

Enter the

password as root.

You wil l need to

store these

credentials as

you need them to

access MySQL.



<a name="br12"></a> 

Enter the

password. You wil l

need to store

Windows Service

these

as yo

to acc

name is MYSQL80,

click next



<a name="br13"></a> 



<a name="br14"></a> 



<a name="br15"></a> 

Enter the

password you

have set in

previous step and

click check to

connect with

MySQL server.



<a name="br16"></a> 

Now, the

installation is

completed.

.



<a name="br17"></a> 

**Post Installation…**

• Af ter the installation, we can monitor MySQL server by accessing MySQL

notifier f rom the task bar.

• If MySQL notifier is not installed, download it by clicking on the link

[https://downloads.mysql.com/archives/notifier](https://downloads.mysql.com/archives/notifier/)[/](https://downloads.mysql.com/archives/notifier/)

• Through the MySQL notif ier, we could start, stop or restart MySQL

components.



<a name="br18"></a> 

• To open the W orkbench, where we write and execute several queries, we

should click on “SQL Editor”.

Now, the

installation is

completed.

.

• Once the workbench is opened, we need to enter the credentials ( used

during installation) to access workbench. Following screenshot exhibits the

same.



<a name="br19"></a> 

Enter the password

used while

installation.



<a name="br20"></a> 

**Executing queries in MySQL Workbench**

Goto File and select “New Query Tab “ to write and execute the queries.



<a name="br21"></a> 

**Executing queries using a Java Application**

Now let us write and execute the SQL queries using a Java Application.

How do we do it?

-> By using a JDBC Driver. JDBC stands for Java Database Connecti vit y.



<a name="br22"></a> 

**JDBC Driver Types**

**Type 1:** JDBC-ODBC Bridge driver (Bridge)

**Type 2:** Native-API/partly Java driver (Native)

**Type 3:** All Java/Net-protocol driver (Middleware)

**Type 4:** All Java/Native-protocol driver (Pure).

We will be using the Type 4 driver , as we use

libraries to communicate directly with the

database server.



<a name="br23"></a> 

**Download the Jar file:**

We need a jar file mysql-connector-java-8.0.26.jar to compile and execute a

application. If you want to compile the examples f rom the command line, go to

the site <https://downloads.mysql.com/archives/c-j/>[ ](https://downloads.mysql.com/archives/c-j/)and download the MySQL

connector.

Select this

Driver



<a name="br24"></a> 

By default the mysql connector

jar file is downloaded along with

Mysql Server, Workbench etc. It

is located in the following

directory:

C:\Program Files

(x86)\MySQL\Connector J 8.0



<a name="br25"></a> 

Copy this mysql connector jar

file and paste it inside

C:\apache-tomcat-9.0.52\lib



<a name="br26"></a> 

**Steps to Execute the application**

**Option 1**: Executing the Program by adding the jar file path in a bat file .

Add the whole path for jar file in CLASSPATH inside your env-setup.bat file

The location of the JAR files highlighted will differ based on where they are present on your computer

Please make sure you do the changes accordingly

Executing by

adding jar file in

class path in

env-setup.bat file



<a name="br27"></a> 

**Option 2** : By setting a classpath variable.

Steps:

• Goto Control Panel -> system ->

Advanced

system settings

->

Environment Variabl es .

• Under Us er variables, choose n ew, and

create a new variable called

Classpath = “The full

pathname wher e

jar file is pres ent

in the system “

• Click on save.

• Then OK.



<a name="br28"></a> 

**A walkthrough example**

In this example,

• First, we will create a database called “exa m pledatabase” using

MySQL workbench.

• Secondly, we will create a table “Registratio n” within the

exampledatabase and store customer login details

• Third, we will create a table “CustomerOrders” within the

exampledatabase and sto re o rder details fo r game speed

application.



<a name="br29"></a> 

**A walkthrough example**

• ***Step 1***: Create a database called “exampledat abas e” in the workbench

space, and execu te the SQL command.

Query to create a

new database



<a name="br30"></a> 

**A walkthrough example**

Write and execute the following commands to check if the database is created.

-> show databases;

Our

Exampledatabase is

created



<a name="br31"></a> 

***Step 2***: Create a table “Registration” in the workbench space,

and execute the SQL command.



<a name="br32"></a> 

***Step 3***: Create a table called “CustomerOrder” in the workbench space,

and execute the SQL command.

Specify the id as primary key for table



<a name="br33"></a> 

**Example –Registration**

• New User can Register into Website by Clicking on the Register here

link On clicking the button user is directed to Registration page



<a name="br34"></a> 

• User provides the login information

• On clicking create user button data is stored in Registration Table of My

sql



<a name="br35"></a> 

• User data is stored in Registration table you can check using the select

query in workbench to check if all the column values are stored

properly



<a name="br36"></a> 

• After an Account is created for user in Registration table user can

login into website with the credentials



<a name="br37"></a> 

**Example –Place Order**

• Click on the products available in the navigatio n bar

• Yo u can also select the products from the left navigat ion bar



<a name="br38"></a> 

**Example – Place Order:**

• Clicking on a product type will take you to the product page

• You have different options available such as buy a product , write reviews.



<a name="br39"></a> 

**Example – Place Order:**

• Click on ‘Buy’ button on the products page to purchase the product

• This should take you to a new page (Cart Servlet) where you can

purchase the product

• Click on ‘Check Out’ to place the order for the selected product.



<a name="br40"></a> 

**Example – Place Order:**

• Clicking on CheckOut Button will take you to the CheckOut webpage

where you have to provide your credit card no and address information.



<a name="br41"></a> 

**Example – Place Order:**

Order is Deleted

from the cart

• On clicking the submit button from check out page

order will be stored in My Sql database and order no

will be generated



<a name="br42"></a> 

**Example – Place Order:**

You can Check if the order Stored by executing select Query in database

using sql workbench



<a name="br43"></a> 

**Servlets MySql Connection**

• We will be using com.mysql.jdbc.Driver for connecting mysql from

servlets

~~Syntax:~~

Connection conn=

Class.forName("com.mysql.jdbc.Driver").newInstance();

DriverMana ger.*getConnection() method is used to connect to my sql*

*database*

Specify the database url , user name and password as parameter to the

getConnection() method

conn=DriverManager.*getConnection("jdbc:mysql://localhost:3306/exampleda*

*tabase","root",“root");*



<a name="br44"></a> 

**Prepared Statement Execution**

• Prepared Statement are used to generate Sql statement for a Query

String in java

• Syntax:

Prepared Statement ps=conn.prepareStatement(“select \* from

Registra tio n where username=? And usertype=?”)

• Specify the Query String as parameter inside conn.prepareStatement() to

perform insert or select in to database from java

• ? Are place holder where we need to provide the value for a particular

query

• In the next line ? We will replace with actual parameter value As

ps.setStr ing(1 ,”c ustom er 1 ”) –1 denotes the first ? Place

ps.setString(2,”customer ”) – 2 denotes the second ? Place



<a name="br45"></a> 

W alk through to get connect

to Database from Servlet



<a name="br46"></a> 

**MySqlDataStoreUtilities class to connect Database from Servlet**

public class MySqlDataStoreUtilities

{

Connection conn = null;

public void getConnection()

{

try

{

Class.forName("com.mysql.jdbc.Driver").newInstance();

conn=

DriverManager.getConnection("jdbc:mysql://localhost:3306/exampledatabase“

,"root",“root");

}

catch(Exception e)

{}

Connecting to

example

}

database



<a name="br47"></a> 

W alkthrough for

User

Registration

Code Snippet



<a name="br48"></a> 

**User Registration Sample Code**

HashMap<String, User> hm=new HashMap<String, User>();

try

{

hm=MySqlDataStoreUtilities.selectUser();

}

Calling utility function

to select data from

database and storing

orders in hashmap

catch(Exception e){}

if(hm.containsKey(username))

error\_msg = "Username already exist as " + usertype;

else

{

User user = new User(username,password,usertype);

hm.put(username, user);

MySqlDataStoreUtilities.insertUser(…);

}

Calling utility function

to insert user details in

database



<a name="br49"></a> 

**Utility Function For Registration**

public static void insertUser(String username,String password,String usertype){

try{

Class.forName("com.mysql.jdbc.Driver").newInstance();

conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/exampleda

tabase“,”root”,”root”)

Connecting to

//getConnection();

example

database

String insertIntoCustomerRegisterQuery = "INSERT INTO

Registration(username,password,usertype) "

\+ "VALUES (?,?,?);";

Query to insert

data to table

PreparedStatement pst =

conn.prepareStatement(insertIntoCustomerRegisterQuery);

pst.setString(1,username);

pst.setString(2,password);

pst.setString(3,usertype);

pst.execute();

Setting Value for Each

Parameter

}

Execute method will

insert data into

database

catch(Exception e){}

}



<a name="br50"></a> 

Walkthro u g h

for Inserti n g

Order Code

Snippet



<a name="br51"></a> 

**Storing Order Payments**

public void storePayment(int orderId,String orderName,double orderPrice,String

userAddress,String creditCardNo){

HashMap<Integer, ArrayList<OrderPayment>> orderPayments= new HashMap<Integer,

ArrayList<OrderPayment>>(); try

{orderPayments= MySqlDataStoreUtilities.selectOrder();

Calling utility function

}

to select data from

database and storing

orders in hashmap

catch(Exception e){}

if(!orderPayments.containsKey(orderId)){

ArrayList<OrderPayment> arr = new ArrayList<OrderPayment>();

orderPayments.put(orderId, arr);

}

ArrayList<OrderPayment> listOrderPayment = orderPayments.get(orderId)

OrderPayment orderpayment = new OrderPayment (…);

listOrderPayment.add(orderpayment);

try

Calling utility function

to inserting orders in

database

{MySqlDataStoreUtilities.insertOrder(…);

}}



<a name="br52"></a> 

**Utility Function for Select Order into hashmap**

public static HashMap<Integer, ArrayList<OrderPayment>> selectOrder()

{

HashMap<Integer,ArrayList<OrderPayment>> orderPayments=new HashMap<Integer,ArrayList<OrderPayment>>();

try{

getConnection();

ResultSet used to

store table data

obtained from

String selectOrderQuery ="select \* from customerorders";

PreparedStatement pst = conn.prepareStatement(selectOrderQuery);

ResultSet rs = pst.executeQuery();

database in servlet

ArrayList<OrderPayment> orderList=new ArrayList<OrderPayment>();

while(rs.next())

{

Iterate through

ResultSet and Store

each order into class

object

if(!orderPayments.containsKey(rs.getInt("OrderId")))

{

ArrayList<OrderPayment> arr = new ArrayList<OrderPayment>();

orderPayments.put(rs.getInt("orderId"), arr);

}

ArrayList<OrderPayment> listOrderPayment =orderPayments.get(rs.getInt("OrderId"));

OrderPayment order= new

OrderPayment(rs.getInt("OrderId"),rs.getString("userName"),rs.getString("orderName“));

listOrderPayment.add(order);

}

}catch(…){}

return orderPayments;}



<a name="br53"></a> 

**Utility Function for storing orders**

public static void insertOrder(int orderId,String userName,String orderName)

{ try

{

Class.forName("com.mysql.jdbc.Driver").newInstance();

conn =

DriverManager.getConnection("jdbc:mysql://localhost:3306/exampledatabase“

,”root”,”root”);

Connecting to

String insertIntoCustomerOrderQuery = "INSERT INTO

customerOrders(OrderId,UserName,OrderName) “ + "VALUES (?,?,?);";

example

database

PreparedStatement pst =

conn.prepareStatement(insertIntoCustomerOrderQuery);

Query to insert

data to table

pst.setInt(1,orderId);

pst.setString(2,userName);

Setting Value for Each

Parameter

pst.setString(3,orderName);

pst.execute();

}

Execute method will

insert data into

database

catch(Exception e){}

}



<a name="br54"></a> 

QUESTIONS?

