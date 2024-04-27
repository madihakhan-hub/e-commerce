# E-Commerce Website

## Description

This project is an e-commerce website backend built using Express.js, Sequelize ORM, and MySQL database. It provides a RESTful API for managing categories, products, and tags. The API allows users to perform CRUD operations to create, read, update, and delete data related to categories, products, and tags. The project also includes database seeding scripts to populate the database with initial data.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Database Schema](#database-schema)
- [Seeding Data](#seeding-data)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory:

   ```bash
   cd e-commerce-backend
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Configure environment variables:

   Create a `.env` file in the root directory and provide the following variables:

   ```plaintext
   DB_NAME=your_database_name
   DB_USER=your_database_username
   DB_PW=your_database_password
   ```

5. Set up MySQL database:

   Create the database using the provided schema.sql file:

   ```bash
   mysql -u <username> -p < schema.sql
   ```

6. Run database migrations:

   ```bash
   npm run migrate
   ```

## Usage

1. Start the server:

   ```bash
   npm start
   ```

2. Test the API endpoints using tools like Insomnia Core or Postman. Refer to the [API Endpoints](#api-endpoints) section for details on available endpoints and their usage.

## API Endpoints

The API provides the following endpoints:

- `GET /api/categories`: Get all categories.
- `GET /api/categories/:id`: Get a single category by ID.
- `POST /api/categories`: Create a new category.
- `PUT /api/categories/:id`: Update a category by ID.
- `DELETE /api/categories/:id`: Delete a category by ID.

- `GET /api/products`: Get all products.
- `GET /api/products/:id`: Get a single product by ID.
- `POST /api/products`: Create a new product.
- `PUT /api/products/:id`: Update a product by ID.
- `DELETE /api/products/:id`: Delete a product by ID.

- `GET /api/tags`: Get all tags.
- `GET /api/tags/:id`: Get a single tag by ID.
- `POST /api/tags`: Create a new tag.
- `PUT /api/tags/:id`: Update a tag by ID.
- `DELETE /api/tags/:id`: Delete a tag by ID.

Refer to the source code and documentation for more details on request payloads and response formats for each endpoint.

## Database Schema

The database schema includes the following tables:

- `category`: Stores category information.
- `product`: Stores product information.
- `tag`: Stores tag information.
- `product_tag`: Stores the many-to-many relationship between products and tags.

## Seeding Data

The project includes seed files to populate the database with initial data for categories, products, tags, and the product-tag relationship. To seed the database, run the following commands:

```bash
npm run seed
```

This will execute the seed scripts and populate the database with initial data.

## Contributing

Contributions are welcome! If you have suggestions, bug reports, or feature requests, please open an issue or submit a pull request.

