I assumed that there is also a database that I can access through postman

List of products 
  - check if there are correct info (name, description, price..) 

```
GET /api/products
```

Filtering by category
  -  check filtering options and confirm that the response is expected result
```
GET https://automationteststore.com/api/products?category=fragrance
```

Sorting
  - Test sorting options (Date Old > New, Price Low > High, Name A - Z) and verify that the order is correct in the response

```
GET https://automationteststore.com/api/products?sort=price_desc
```

Handling errors
  - Ensure that appropriate error codes and messages are returned

```
GET https://automationteststore.com/api/products/invalid_id
```
```
POST https://automationteststore.com/api/orders
{
  "user_id": "user1",
  "products": [
    {"product_id": "invalid_product_id", "quantity": 1}
  ]
}
```

Placing order 
  - testing if it is possible to place a new order

```
POST https://automationteststore.com/api/orders
{
  "user_id": "user1",
  "products": [
    {"product_id": "prod1", "quantity": 2},
    {"product_id": "prod2", "quantity": 1}
  ]
}
```
Authentication Check:

  - test with an unauthenticated request and ensure it is denied.


I assumed that there is also a database that I can access through postman and these would be some of the text cases: 

Successful User Registration:

```
POST https://example.com/api/register
{
  "username": "user1",
  "email": "user1@gmail.com",
  "password": "SecureP@ssword123"
}
```

Attempting to register with an existing email

```
POST https://example.com/api/register
{
  "username": "user1",
  "email": "user1@gmail.com",
  "password": "SecureP@ssword123"
}
```