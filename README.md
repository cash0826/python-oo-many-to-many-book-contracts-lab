# Many-to-many Object Relationships Lab

## Instructions

### Task

Build a model a many to many relationship between Books and Authors:

* Build Book class
* Build Author class
* Build Contract class
* Build connecting methods between all

### Design

#### Book:
* Attributes:
  * title (string)
  * all (array) 
* Methods:
  * contracts()
  * authors()

#### Authors:
* Attributes:
  * name (string)
  * all (array)
* Methods:
  * contracts()
  * books()
  * sign_contracts(book,date,royalties)
  * total_royalties()

#### Contracts:
* Attributes:
  * author (Author class), 
  * book (Book class), 
  * date (string), 
  * royalties (integer)
  * all (array)
* Methods:
  * contracts_by_date()

### Methods

* `__init__`: title
* Class attributes- all
* Methods:
  * contracts()- This method should return a list of related contracts
  * authors()- This method should return a list of related authors using the Contract class as an intermediary

* `__init__`: name (string)
* Class attributes- all
* Methods:
  * contracts()- This method should return a list of related contracts
  * books()- This method should return a list of related books using the Contract class as an intermediary
  * sign_contracts(book,date,royalties)- This method should create and return a new Contract object between the author and the specified book with the specified date and royalties
  * total_royalties()- This method should return the total amount of royalties that the author has earned from all of their contracts

* `__init__`:
  * author
  * book
  * date 
  * royalties 
* Class attributes: all
* Properties: All properties should raise an exception if not valid
  * author: Is an instance of Author class
  * book:  Is an instance of Book class
  * date: Is an instance of a str
  * royalties:  Is an instance of an int
* Class Methods: contracts_by_date()- This method should return all contracts that have the same date as the date passed into the method

