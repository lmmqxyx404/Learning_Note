# watch out
first you must start the mysql service, then you can connect it.

# In windows,first you must start up mysql service
net start mysql
net stop mysql

# some frequent command
mysql -u root -p
show databases;   
use tablename;
select database();
create table tablename(
  id type(4 length ) not null primary key auto_increment,
  year date
)                     
: create a table

source pathname; //The path should be originated from the root 
drop table tablename  //delete the table
insert into tablename values (value); // create
delete from tablename where condition;  //delete
update tablename set attr='new value',… where condition  //update
select * from tablename where condition  //Retrieve
## rename
rename table previous tablename to latest tablename;
## exit
exit
## show mysql port
show global variables like 'port';

watch out:
when you attempt to import a backup sql to a new environment, you should install mysql.
Then you should create a database and use it.At last, you can use source command.