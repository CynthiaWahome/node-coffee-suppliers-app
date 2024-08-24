
---

# Coffee Suppliers App

## Overview

The Coffee Suppliers App is a simple CRUD (Create, Read, Update, Delete) application built with Express.js. It allows for the management of supplier information in a coffee business. This application demonstrates basic database operations and provides a foundation for further development.

## Local Setup

### 1. Set Up the Database

First, create the local database and table by executing the following SQL commands. This step sets up a database named `coffee` and a table named `suppliers`.

```sql
CREATE DATABASE IF NOT EXISTS coffee;
USE coffee;

CREATE TABLE IF NOT EXISTS suppliers (
  id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(255) NOT NULL,
  address VARCHAR(255) NOT NULL,
  city VARCHAR(255) NOT NULL,
  state VARCHAR(255) NOT NULL,
  email VARCHAR(255) NOT NULL,
  phone VARCHAR(100) NOT NULL,
  PRIMARY KEY (id)
);
```

### 2. Install Dependencies and Run the Application

Follow these steps to set up and run the application locally:

1. **Install Dependencies**

   Use npm to install the necessary packages:

   ```bash
   npm install -y
   ```

2. **Configure Environment Variables**

   Set your database connection variables before starting the server. You can define these variables in your terminal session or use a `.env` file.

   **Setting Environment Variables in the Terminal:**

   ```bash
   APP_DB_HOST=localhost \
   APP_DB_USER=root \
   APP_DB_PASSWORD="" \
   APP_DB_NAME=coffee \
   npm start
   ```

   **Using a `.env` File:**

   Create a `.env` file in the root directory of your project with the following content:

   ```env
   APP_DB_HOST=localhost
   APP_DB_USER=root
   APP_DB_PASSWORD=""
   APP_DB_NAME=coffee
   ```

   Then, start the server with:

   ```bash
   npm start
   ```

   If environment variables are not set, the application will default to the values specified in `app/config/config.js`.

## Configuration

Database configuration is managed in `app/config/config.js`. You can adjust the default settings here if needed.

## License

This project is licensed under the [MIT License](LICENSE). See the LICENSE file for more details.

---