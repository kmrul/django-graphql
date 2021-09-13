# django-graphql

## How to run django-graphql project

** Step 1: **
Clone this repository:
``` git clone https://github.com/kmrul/django-graphql.git ```
```
cd django-graphql
pip install virtualenv
virtualenv env

```

** Step 2 **
Activate virtual environement
** Mac OS/Linux **
```
source env/bin/activate
```
** Windows **
```
env\Scripts\activate
```
** Step 3 **
Install Python Packages

``` 
pip install -r requirements.txt
```

** Step 4 **
Make migrations 
```
python manage.py makemigrations
python manage.py migrate

```
Then run application 
```
python manage.py runserver
```
Browse http://120.0.0.1:8000/graphql 

** Step 5 **
Testing our GraphQL API

```
Schema For books:

{
  books{
      id
      title
      author
      isbn
      pages 
      price
      quantity
      description
      status
    }
}

Schema For categories:

{
  categories{
    id,
    title
  }
}

```

Mutation
```
Mutation for category

mutation {
 create_category:createCategory(title :"Fruits") {
  category {
   id,
   title,
  }
 }
}

Mutation for Book:

mutation {
  create_book: createBook(input: {title:"My favorite books",author: "Kamrul Hasan", pages: 12, price: 100, quantity: 5, description:"this is brief description", status: "True"}){
    book {
      id,
      title,
      author,
      pages,
      price,
      quantity,
      description,
      status
    }
  }
}

```

** Happy Django Graphql **