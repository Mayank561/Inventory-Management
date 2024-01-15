# Inventory Management System

## Table of Contents
1. [API Integration](#api-integration)
2. [Project Setup](#project-setup)
3. [External Libraries and Tools](#external-libraries-and-tools)

## API Integration<a name="api-integration"></a>

### User Registration

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

- `name`: User's name (min length: 6 characters)
- `email`: User's email (should be a valid email format)
- `password1`: User's password (min length: 9 characters)
- `password2`: Confirm password (min length: 9 characters)
- `usertype`: User type

**Response:**

- If successful, redirects to the login page with a success message.
- If the email already exists, an alert is shown.
- If there's any other error, an alert with "Something Wrong" is shown.

### User Login

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

- `log_email`: User's email
- `log_password`: User's password

**Response:**

- If the user is not registered, shows an error message.
- If the password is incorrect, shows an error message.
- If successful, redirects to the dashboard.

### Category Management

#### Fetch Categories

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "getCategory": 1
}
**Response:**

Populates the category dropdowns with the fetched categories.

#### Add Category

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "category_name": "New category name"
}
**Response:**

Populates the category dropdowns with the fetched categories.

#### Add Category

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "category_name": "New category name"
}
**Response:**

- If successful, shows a success message.
- If there's an error, shows an alert with the error.

#### Update Category

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "updateCategory": 1,
  "id": "Category ID",
  "update_category": "Updated category name",
  "parent_cat": "Parent category ID"
}

**Response:**

- Redirects to the current page after updating.

#### Brand Management

#### Fetch Brands

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "getBrand": 1
}
**Response:**

- Populates the brand dropdown with the fetched brands.

#### Add Brand

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "brand_name": "New brand name"
}
**Response:**

- If successful, shows a success message.
- If there's an error, shows an alert with the error.

#### Update Brand

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "updateBrand": 1,
  "id": "Brand ID",
  "update_brand": "Updated brand name"
}
**Response:**

- Redirects to the current page after updating.

#### Delete Brand

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "deleteBrand": 1,
  "id": "Brand ID"
}
**Response:**

- Shows an alert for success or error.

#### Product Management

##### Fetch Products

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "manageProduct": 1,
  "pageno": "Page number for pagination"
}
**Response:**

- Displays the product table.

##### Add Product

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "product_name": "Product name",
  "cid": "Category ID",
  "bid": "Brand ID",
  "product_price": "Product price",
  "product_stock": "Product stock quantity"
}
**Response:**

- If successful, shows a success message.
- If there's an error, shows an alert with the error.

##### Update Product

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "updateProduct": 1,
  "id": "Product ID",
  "update_product": "Updated product name",
  "select_cat": "Updated category ID",
  "select_brand": "Updated brand ID",
  "product_price": "Updated product price",
  "product_qty": "Updated product stock quantity"
}
**Response:**

- If successful, shows a success message.
- If there's an error, shows an alert with the error.

##### Delete Product

**Endpoint:** `/includes/process.php`  
**Method:** `POST`

**Data:**

```json
{
  "deleteProduct": 1,
  "id": "Product ID"
}
**Response:**

- Shows an alert for success or error.

## Project Setup<a name="project-setup"></a>

1. Clone the project repository.
2. Set up a web server (e.g., Apache) and configure it to point to the project directory.
3. Import the database schema from the provided SQL file.
4. Update the 'DOMAIN' variable in the JavaScript files to match your server configuration.
5. Access the project via the web server.

## External Libraries and Tools<a name="external-libraries-and-tools"></a>

1. **jQuery:** Used for simplifying AJAX requests and DOM manipulation.
2. **Bootstrap:** Used for styling and layout components.
3. **FPDF (Free PDF):** Used for generating PDF documents.




