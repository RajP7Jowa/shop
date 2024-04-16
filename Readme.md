Sure, here's the updated README with the database structure:

---

# Product Management System

Welcome to the Product Management System! This system allows administrators to manage products and display them to the public.

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your_username/product-management-system.git
```

### 2. Set Up Virtual Environment

```bash
python -m venv venv
```

### 3. Activate Virtual Environment

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Set Up Database

- Create a MySQL database named `product_management_system`.
- Import the `product_management_system.sql` file located in the `database` directory to initialize the database schema and sample data.

### 6. Update Database Configuration

Update the database connection details in `app.py`:

```python
db = mysql.connector.connect(
    host='localhost',
    user='your_mysql_username',
    password='your_mysql_password',
    database='product_management_system'
)
```

### 7. Run the Application

```bash
python app.py
```

### 8. Access the Application

Navigate to `http://localhost:5000` in your web browser.

## Usage

### Admin Interface

- Navigate to `http://localhost:5000/login` to access the admin login page.
- Use the default admin credentials: Username: `admin`, Password: `1234`.
- Once logged in, you can add, edit, and delete products using the admin dashboard at `http://localhost:5000/admin`.

### Public Interface

- The public interface displays the list of available products.
- Access the public interface at `http://localhost:5000/`.
- Click on a product to view its details, including an option to contact via WhatsApp for purchase inquiries.

## Database Structure

The database structure consists of the following tables:

- `products`: Stores information about products, including name, price, description, image path, and WhatsApp number for purchase inquiries.

```sql
CREATE TABLE products (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    price DECIMAL(10, 2) NOT NULL,
    description TEXT,
    image_path VARCHAR(255)
);
```

## Dependencies

- Flask: Web framework for building the application.
- MySQL Connector: Python driver for MySQL database connection.
- Bootstrap: Frontend framework for styling.

## Contributing

Contributions are welcome! Please fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to customize this README to fit your project's specific details and requirements!