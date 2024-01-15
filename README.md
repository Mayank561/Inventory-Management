This project is a simple inventory management system with features like user registration, login,category management, brand management, product management, and order processing. it uses a web-based interface for users to interact with the system.

# Table of contents
1. API Intregation
2. project setup
3. external libaries and Tools


# Endpint: '/includes/process.php'
Method: 'post'
name: User's name (min length: 6 characters)
email: User's email (should be a valid email format)
password1: User's password (min length: 9 characters)
password2: Confirm password (min length: 9 characters)
usertype: User type

# Response:
If successful, redirects to the login page with a success message.
If the email already exists, an alert is shown.
If there's any other error, an alert with "Something Wrong" is shown.

# User Login
Endpoint: '/includes/process.php'

# parameters:
log_email: User's email
log_password: User's password


# Response:

If the user is not registered, shows an error message.
If the password is incorrect, shows an error message.
If successful, redirects to the dashboard.

# Category Management
Fetch Categories
Endpoint: /includes/process.php

Method: POST

Data:

getCategory: 1

# Response:

Populates the category dropdowns with the fetched categories.
Add Category
Endpoint: /includes/process.php

# Method: POST

Data:

category_name: New category name
Response:

If successful, shows a success message.
If there's an error, shows an alert with the error.

# Update Category

# Endpoint: /includes/process.php

Method: POST

Data:

updateCategory: 1
id: Category ID
update_category: Updated category name
parent_cat: Parent category ID


Response:

Redirects to the current page after updating.
Delete Category
Endpoint: /includes/process.php

Method: POST

Data:

deleteCategory: 1
id: Category ID
Response:

Shows an alert for success, dependency, or error.
Brand Management
Fetch Brands
Endpoint: /includes/process.php

Method: POST

Data:

getBrand: 1
Response:

Populates the brand dropdown with the fetched brands.
Add Brand
Endpoint: /includes/process.php

Method: POST

Data:

brand_name: New brand name
Response:

If successful, shows a success message.
If there's an error, shows an alert with the error.
Update Brand
Endpoint: /includes/process.php

Method: POST

Data:

updateBrand: 1
id: Brand ID
update_brand: Updated brand name
Response:

Redirects to the current page after updating.
Delete Brand
Endpoint: /includes/process.php

Method: POST

Data:

deleteBrand: 1
id: Brand ID
Response:

Shows an alert for success or error.
Product Management
Fetch Products
Endpoint: /includes/process.php

Method: POST

Data:

manageProduct: 1
pageno: Page number for pagination
Response:

Displays the product table.
Add Product
Endpoint: /includes/process.php

Method: POST

Data:

product_name: Product name
cid: Category ID
bid: Brand ID
product_price: Product price
product_stock: Product stock quantity
Response:

If successful, shows a success message.
If there's an error, shows an alert with the error.
Update Product
Endpoint: /includes/process.php

Method: POST

Data:

updateProduct: 1
id: Product ID
update_product: Updated product name
select_cat: Updated category ID
select_brand: Updated brand ID
product_price: Updated product price
product_qty: Updated product stock quantity
Response:

If successful, shows a success message.
If there's an error, shows an alert with the error.
Delete Product
Endpoint: /includes/process.php

Method: POST

Data:

deleteProduct: 1
id: Product ID
Response:

Shows an alert for success or error.



2. project setup

1. clone the project repository.
2. set up web server(e.g.,Apache) and condigure it to point the project directory.
3. Import the database schema for the provided SQL file.
4. upate the 'DOMAIN' variable in the javascript files to match your server condiguration.
5. Access the project via the web server.


3. External Libraries
   1. jQuery: Used for simplifying AJAX requests and DOM manipulation.
   2. Bootstrap: Used for styling and layout components.
   3. FPDF(Free PDf): Used for genrating PDF documents.





