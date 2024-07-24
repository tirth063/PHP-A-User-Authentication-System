#SQL TABLE
``` -- Users Table
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    firstname VARCHAR(50) NOT NULL,
    lastname VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    mobilenumber VARCHAR(15) NOT NULL,
    password VARCHAR(255) NOT NULL,
    token VARCHAR(255) NOT NULL,
    is_active TINYINT(1) DEFAULT 0,
    date_time DATETIME DEFAULT CURRENT_TIMESTAMP
);

--add an index on the email and token columns for faster lookups
CREATE INDEX idx_email ON users (email);
CREATE INDEX idx_token ON users (token); ```
