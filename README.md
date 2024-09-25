**E-Commerce Web Application**
This Spring Boot application provides a REST API for managing products in an e-commerce store. Key features include:

**Product Management:**
CRUD (Create, Read, Update, Delete) operations for products.

Product image storage and retrieval.

Basic search functionality for products (name, description, brand, category).

**Technologies:**

Spring Boot

Spring Data JPA(hibernate),

Lombok (for concise boilerplate code).

**Prerequisites:**
Java Development Kit (JDK) installed
h2 database server running
Maven build tool

**Configuration:**
Update application.properties with your database connection details (URL, username, password).

**API Reference**

**Product API:**
Endpoint: http://localhost:8080/api/products

**Supported methods:**
GET: Retrieves all products (paginated results can be implemented).
GET with ID (e.g., /api/products/1): Retrieves a specific product by ID.
POST: Creates a new product.
PUT with ID: Updates an existing product.
DELETE with ID: Deletes a product.

**Image handling:**
Product creation (POST) accepts a multipart request with a product object and an image file.
Product update (PUT) can accept an image file for updates.
GET with product ID /image retrieves the product's image.

**Search API:**
Endpoint: http://localhost:8080/api/products/search?keyword={keyword}
Supported method:
GET: Searches products based on the provided keyword (name, description, brand, category).
Example Usage

**Get all products:**

**Method: GET**
URL: http://localhost:8080/api/products
Get product by ID (replace 1 with your product ID):

**Method: GET**
URL: http://localhost:8080/api/products/1
Create a new product:

**Method: POST**
Body: JSON object representing the product (including name, description, brand, category, etc.)
Multipart form data: Include an image file for the product.
Update a product (replace 1 with your product ID):

**Method: PUT**
URL: http://localhost:8080/api/products/1
Body: JSON object representing product updates (optional)
Multipart form data: Include an image file for updates (optional)
Delete a product (replace 1 with your product ID):

**Method: DELETE**
URL: http://localhost:8080/api/products/1
Search products by keyword:

**Method: GET**
URL: http://localhost:8080/api/products/search?keyword=electronics
