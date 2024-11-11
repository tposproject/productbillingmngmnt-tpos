Step:1

Required softwares to install:
intellij community edition,
jdk17,
maven,
postman,
mysql

Step2:

Open mysql In database run create database TPOS;

Step3:

First clone the project and build (mvn clean install) and run the project. Capture the posrt number from the consolehttp://localhost:8844/userregister  or http://localhost:8844/adminregister 


Step:4

Below are the queries to run in database
-- Insert Categories
INSERT INTO Category (name) VALUES ('Electronics');
INSERT INTO Category (name) VALUES ('Groceries');
INSERT INTO Category (name) VALUES ('Clothing');
INSERT INTO Category (name) VALUES ('Furniture');
INSERT INTO Category (name) VALUES ('Beauty');
INSERT INTO Category (name) VALUES ('Toys');
INSERT INTO Category (name) VALUES ('Books');
INSERT INTO Category (name) VALUES ('Sports');
INSERT INTO Category (name) VALUES ('Home Appliances');
INSERT INTO Category (name) VALUES ('Jewelry');
INSERT INTO Category (name) VALUES ('Garden');
INSERT INTO Category (name) VALUES ('Automotive');
INSERT INTO Category (name) VALUES ('Tools');
INSERT INTO Category (name) VALUES ('Pet Supplies');
INSERT INTO Category (name) VALUES ('Office Supplies');

-- Insert Products for each category (10 products per category)
-- Assuming your 'Product' table has columns: id, name, price, quantity, category_id

-- Electronics
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Smartphone', 699.99, 50, (SELECT id FROM Category WHERE name = 'Electronics'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Laptop', 999.99, 30, (SELECT id FROM Category WHERE name = 'Electronics'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Tablet', 499.99, 20, (SELECT id FROM Category WHERE name = 'Electronics'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Smartwatch', 199.99, 60, (SELECT id FROM Category WHERE name = 'Electronics'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Camera', 350.00, 40, (SELECT id FROM Category WHERE name = 'Electronics'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Bluetooth Speaker', 80.00, 100, (SELECT id FROM Category WHERE name = 'Electronics'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Gaming Console', 400.00, 25, (SELECT id FROM Category WHERE name = 'Electronics'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Headphones', 150.00, 80, (SELECT id FROM Category WHERE name = 'Electronics'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('TV', 799.99, 10, (SELECT id FROM Category WHERE name = 'Electronics'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Router', 120.00, 35, (SELECT id FROM Category WHERE name = 'Electronics'));

-- Groceries
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Apples', 3.00, 100, (SELECT id FROM Category WHERE name = 'Groceries'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Bananas', 1.50, 150, (SELECT id FROM Category WHERE name = 'Groceries'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Milk', 2.00, 80, (SELECT id FROM Category WHERE name = 'Groceries'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Bread', 1.75, 90, (SELECT id FROM Category WHERE name = 'Groceries'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Rice', 10.00, 50, (SELECT id FROM Category WHERE name = 'Groceries'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Eggs', 2.50, 200, (SELECT id FROM Category WHERE name = 'Groceries'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Chicken Breast', 7.99, 60, (SELECT id FROM Category WHERE name = 'Groceries'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Butter', 3.50, 70, (SELECT id FROM Category WHERE name = 'Groceries'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Pasta', 1.99, 120, (SELECT id FROM Category WHERE name = 'Groceries'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Cereal', 4.50, 50, (SELECT id FROM Category WHERE name = 'Groceries'));

-- Clothing
INSERT INTO Product (name, price, quantity, category_id) VALUES ('T-shirt', 15.00, 100, (SELECT id FROM Category WHERE name = 'Clothing'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Jeans', 40.00, 60, (SELECT id FROM Category WHERE name = 'Clothing'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Jacket', 100.00, 30, (SELECT id FROM Category WHERE name = 'Clothing'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Socks', 5.00, 200, (SELECT id FROM Category WHERE name = 'Clothing'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Dress', 50.00, 50, (SELECT id FROM Category WHERE name = 'Clothing'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Skirt', 30.00, 40, (SELECT id FROM Category WHERE name = 'Clothing'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Sweater', 60.00, 70, (SELECT id FROM Category WHERE name = 'Clothing'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Hat', 20.00, 90, (SELECT id FROM Category WHERE name = 'Clothing'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Belt', 25.00, 80, (SELECT id FROM Category WHERE name = 'Clothing'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Shoes', 75.00, 60, (SELECT id FROM Category WHERE name = 'Clothing'));

-- Furniture
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Sofa', 500.00, 10, (SELECT id FROM Category WHERE name = 'Furniture'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Chair', 75.00, 40, (SELECT id FROM Category WHERE name = 'Furniture'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Dining Table', 300.00, 20, (SELECT id FROM Category WHERE name = 'Furniture'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Coffee Table', 150.00, 30, (SELECT id FROM Category WHERE name = 'Furniture'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Wardrobe', 400.00, 15, (SELECT id FROM Category WHERE name = 'Furniture'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Bed', 600.00, 12, (SELECT id FROM Category WHERE name = 'Furniture'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Dresser', 250.00, 18, (SELECT id FROM Category WHERE name = 'Furniture'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Bookshelf', 120.00, 25, (SELECT id FROM Category WHERE name = 'Furniture'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('TV Stand', 200.00, 30, (SELECT id FROM Category WHERE name = 'Furniture'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Nightstand', 80.00, 40, (SELECT id FROM Category WHERE name = 'Furniture'));

-- Beauty
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Lipstick', 15.99, 100, (SELECT id FROM Category WHERE name = 'Beauty'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Foundation', 25.00, 80, (SELECT id FROM Category WHERE name = 'Beauty'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Mascara', 12.00, 60, (SELECT id FROM Category WHERE name = 'Beauty'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Perfume', 50.00, 40, (SELECT id FROM Category WHERE name = 'Beauty'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Nail Polish', 8.00, 120, (SELECT id FROM Category WHERE name = 'Beauty'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Moisturizer', 30.00, 70, (SELECT id FROM Category WHERE name = 'Beauty'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Hair Conditioner', 10.00, 90, (SELECT id FROM Category WHERE name = 'Beauty'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Sunscreen', 20.00, 100, (SELECT id FROM Category WHERE name = 'Beauty'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Shampoo', 15.00, 80, (SELECT id FROM Category WHERE name = 'Beauty'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Eye Shadow', 18.00, 60, (SELECT id FROM Category WHERE name = 'Beauty'));

-- Toys
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Action Figure', 20.00, 150, (SELECT id FROM Category WHERE name = 'Toys'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Doll', 25.00, 120, (SELECT id FROM Category WHERE name = 'Toys'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Building Blocks', 30.00, 100, (SELECT id FROM Category WHERE name = 'Toys'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Toy Car', 10.00, 200, (SELECT id FROM Category WHERE name = 'Toys'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Board Game', 35.00, 50, (SELECT id FROM Category WHERE name = 'Toys'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Stuffed Animal', 15.00, 180, (SELECT id FROM Category WHERE name = 'Toys'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Puzzle', 20.00, 140, (SELECT id FROM Category WHERE name = 'Toys'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Toy Train', 25.00, 60, (SELECT id FROM Category WHERE name = 'Toys'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Remote Control Car', 50.00, 80, (SELECT id FROM Category WHERE name = 'Toys'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Drone', 100.00, 40, (SELECT id FROM Category WHERE name = 'Toys'));

-- Books
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Novel', 12.00, 90, (SELECT id FROM Category WHERE name = 'Books'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Biography', 15.00, 70, (SELECT id FROM Category WHERE name = 'Books'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Science Fiction', 18.00, 60, (SELECT id FROM Category WHERE name = 'Books'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Mystery', 10.00, 100, (SELECT id FROM Category WHERE name = 'Books'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Textbook', 50.00, 40, (SELECT id FROM Category WHERE name = 'Books'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Comic Book', 5.00, 200, (SELECT id FROM Category WHERE name = 'Books'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Cookbook', 25.00, 70, (SELECT id FROM Category WHERE name = 'Books'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('History Book', 30.00, 50, (SELECT id FROM Category WHERE name = 'Books'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Travel Guide', 15.00, 80, (SELECT id FROM Category WHERE name = 'Books'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Self-Help Book', 20.00, 100, (SELECT id FROM Category WHERE name = 'Books'));

-- Sports
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Soccer Ball', 25.00, 60, (SELECT id FROM Category WHERE name = 'Sports'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Basketball', 30.00, 50, (SELECT id FROM Category WHERE name = 'Sports'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Tennis Racket', 80.00, 40, (SELECT id FROM Category WHERE name = 'Sports'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Baseball Glove', 40.00, 30, (SELECT id FROM Category WHERE name = 'Sports'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Golf Clubs', 200.00, 20, (SELECT id FROM Category WHERE name = 'Sports'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Hockey Stick', 60.00, 35, (SELECT id FROM Category WHERE name = 'Sports'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Skateboard', 50.00, 80, (SELECT id FROM Category WHERE name = 'Sports'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Yoga Mat', 20.00, 100, (SELECT id FROM Category WHERE name = 'Sports'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Dumbbells', 35.00, 120, (SELECT id FROM Category WHERE name = 'Sports'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Treadmill', 500.00, 10, (SELECT id FROM Category WHERE name = 'Sports'));

-- Home Appliances
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Washing Machine', 800.00, 10, (SELECT id FROM Category WHERE name = 'Home Appliances'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Refrigerator', 1200.00, 8, (SELECT id FROM Category WHERE name = 'Home Appliances'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Microwave', 150.00, 20, (SELECT id FROM Category WHERE name = 'Home Appliances'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Dishwasher', 600.00, 15, (SELECT id FROM Category WHERE name = 'Home Appliances'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Vacuum Cleaner', 250.00, 30, (SELECT id FROM Category WHERE name = 'Home Appliances'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Air Conditioner', 400.00, 12, (SELECT id FROM Category WHERE name = 'Home Appliances'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Blender', 50.00, 60, (SELECT id FROM Category WHERE name = 'Home Appliances'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Toaster', 30.00, 80, (SELECT id FROM Category WHERE name = 'Home Appliances'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Coffee Maker', 120.00, 40, (SELECT id FROM Category WHERE name = 'Home Appliances'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Iron', 35.00, 50, (SELECT id FROM Category WHERE name = 'Home Appliances'));

-- Jewelry
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Necklace', 100.00, 20, (SELECT id FROM Category WHERE name = 'Jewelry'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Bracelet', 80.00, 25, (SELECT id FROM Category WHERE name = 'Jewelry'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Earrings', 50.00, 40, (SELECT id FROM Category WHERE name = 'Jewelry'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Ring', 150.00, 30, (SELECT id FROM Category WHERE name = 'Jewelry'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Watch', 200.00, 15, (SELECT id FROM Category WHERE name = 'Jewelry'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Brooch', 40.00, 60, (SELECT id FROM Category WHERE name = 'Jewelry'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Pendant', 70.00, 50, (SELECT id FROM Category WHERE name = 'Jewelry'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Cufflinks', 30.00, 100, (SELECT id FROM Category WHERE name = 'Jewelry'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Choker', 90.00, 35, (SELECT id FROM Category WHERE name = 'Jewelry'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Anklet', 25.00, 80, (SELECT id FROM Category WHERE name = 'Jewelry'));

-- Garden
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Lawn Mower', 300.00, 15, (SELECT id FROM Category WHERE name = 'Garden'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Garden Hose', 20.00, 60, (SELECT id FROM Category WHERE name = 'Garden'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Shovel', 25.00, 40, (SELECT id FROM Category WHERE name = 'Garden'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Flower Pots', 10.00, 100, (SELECT id FROM Category WHERE name = 'Garden'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Grass Seed', 30.00, 50, (SELECT id FROM Category WHERE name = 'Garden'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Fertilizer', 25.00, 70, (SELECT id FROM Category WHERE name = 'Garden'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Pruning Shears', 15.00, 80, (SELECT id FROM Category WHERE name = 'Garden'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Watering Can', 12.00, 90, (SELECT id FROM Category WHERE name = 'Garden'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Garden Cart', 40.00, 30, (SELECT id FROM Category WHERE name = 'Garden'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Compost Bin', 60.00, 20, (SELECT id FROM Category WHERE name = 'Garden'));

-- Automotive
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Car Battery', 100.00, 40, (SELECT id FROM Category WHERE name = 'Automotive'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Tire', 150.00, 50, (SELECT id FROM Category WHERE name = 'Automotive'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Engine Oil', 30.00, 70, (SELECT id FROM Category WHERE name = 'Automotive'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Car Wax', 20.00, 100, (SELECT id FROM Category WHERE name = 'Automotive'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Air Filter', 15.00, 80, (SELECT id FROM Category WHERE name = 'Automotive'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Windshield Wipers', 25.00, 60, (SELECT id FROM Category WHERE name = 'Automotive'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Brake Pads', 50.00, 40, (SELECT id FROM Category WHERE name = 'Automotive'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Car Jack', 80.00, 20, (SELECT id FROM Category WHERE name = 'Automotive'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('GPS Navigator', 120.00, 30, (SELECT id FROM Category WHERE name = 'Automotive'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Car Cover', 60.00, 50, (SELECT id FROM Category WHERE name = 'Automotive'));

-- Tools
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Hammer', 15.00, 80, (SELECT id FROM Category WHERE name = 'Tools'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Screwdriver Set', 20.00, 70, (SELECT id FROM Category WHERE name = 'Tools'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Drill', 100.00, 40, (SELECT id FROM Category WHERE name = 'Tools'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Wrench Set', 30.00, 60, (SELECT id FROM Category WHERE name = 'Tools'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Tape Measure', 10.00, 100, (SELECT id FROM Category WHERE name = 'Tools'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Level', 20.00, 90, (SELECT id FROM Category WHERE name = 'Tools'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Utility Knife', 8.00, 150, (SELECT id FROM Category WHERE name = 'Tools'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Plier Set', 25.00, 50, (SELECT id FROM Category WHERE name = 'Tools'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Sander', 60.00, 30, (SELECT id FROM Category WHERE name = 'Tools'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Circular Saw', 150.00, 20, (SELECT id FROM Category WHERE name = 'Tools'));

-- Pet Supplies
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Dog Food', 40.00, 50, (SELECT id FROM Category WHERE name = 'Pet Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Cat Litter', 20.00, 70, (SELECT id FROM Category WHERE name = 'Pet Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Fish Tank', 100.00, 30, (SELECT id FROM Category WHERE name = 'Pet Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Bird Cage', 60.00, 20, (SELECT id FROM Category WHERE name = 'Pet Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Pet Bed', 50.00, 40, (SELECT id FROM Category WHERE name = 'Pet Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Dog Leash', 15.00, 90, (SELECT id FROM Category WHERE name = 'Pet Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Cat Tree', 80.00, 20, (SELECT id FROM Category WHERE name = 'Pet Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Pet Shampoo', 10.00, 100, (SELECT id FROM Category WHERE name = 'Pet Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Hamster Wheel', 30.00, 50, (SELECT id FROM Category WHERE name = 'Pet Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Pet Carrier', 40.00, 60, (SELECT id FROM Category WHERE name = 'Pet Supplies'));

-- Office Supplies
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Notebook', 5.00, 150, (SELECT id FROM Category WHERE name = 'Office Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Pen Set', 10.00, 200, (SELECT id FROM Category WHERE name = 'Office Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Printer', 150.00, 40, (SELECT id FROM Category WHERE name = 'Office Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Paper Ream', 20.00, 100, (SELECT id FROM Category WHERE name = 'Office Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Stapler', 15.00, 80, (SELECT id FROM Category WHERE name = 'Office Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Desk Chair', 120.00, 30, (SELECT id FROM Category WHERE name = 'Office Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Desk Organizer', 25.00, 50, (SELECT id FROM Category WHERE name = 'Office Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Whiteboard', 60.00, 20, (SELECT id FROM Category WHERE name = 'Office Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Marker Set', 12.00, 90, (SELECT id FROM Category WHERE name = 'Office Supplies'));
INSERT INTO Product (name, price, quantity, category_id) VALUES ('Filing Cabinet', 200.00, 10, (SELECT id FROM Category WHERE name = 'Office Supplies'));
