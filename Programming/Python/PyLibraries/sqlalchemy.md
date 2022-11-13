
# Library [[sqlalchemy]]:

***

## About:

- Library developed to work wiht SQL on python. 
- This is ORM - Object Realational Mapper. 
- It provide functionality to work with SQL tables as classes in python.

***

## Get started:

At first we need to install python mysql connector.
```sh
pip install pymysql
pip install sqlalchemy
```


### Create an engine:
	 We use engine co send commands to Database

![[Pasted image 20221026171547.png]]

#### For mysql use:
```py
engine = create_engine(‘mysql://scott:tiger@localhost/foo’)
```
***

## [[PyLibraries]]