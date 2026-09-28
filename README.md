DROP TABLE IF EXISTS users;
DROP TABLE IF EXISTS products;

CREATE TABLE users (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    email TEXT NOT NULL UNIQUE,
    balance REAL NOT NULL DEFAULT 0,
    date_created TEXT NOT NULL
);

CREATE TABLE products (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    price REAL NOT NULL,
    sale REAL NOT NULL DEFAULT 0,
    date_created TEXT NOT NULL
);

INSERT INTO users (id, name, email, balance, date_created) VALUES
(1, 'Иван Петров', 'ivan.petrov@example.com', 12500.50, '2026-09-20'),
(2, 'Анна Смирнова', 'anna.smirnova@example.com', 8400.00, '2026-09-21'),
(3, 'Максим Орлов', 'maxim.orlov@example.com', 3150.75, '2026-09-22'),
(4, 'Елена Волкова', 'elena.volkova@example.com', 17600.00, '2026-09-23'),
(5, 'Дмитрий Соколов', 'dmitry.sokolov@example.com', 5200.25, '2026-09-24');

INSERT INTO products (id, name, price, sale, date_created) VALUES
(1, 'Ноутбук', 89990.00, 10.0, '2026-09-20'),
(2, 'Смартфон', 64990.00, 7.5, '2026-09-21'),
(3, 'Наушники', 12990.00, 15.0, '2026-09-22'),
(4, 'Клавиатура', 7990.00, 5.0, '2026-09-23'),
(5, 'Мышь', 3990.00, 12.0, '2026-09-24');

-- Проверка
SELECT * FROM users;
SELECT * FROM products;
