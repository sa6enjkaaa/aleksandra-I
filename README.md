
-- create
CREATE TABLE EMPLOYEE (

Id INTEGER PRIMARY KEY,
name TEXT NOT NULL,
e_pasts TEXT NOT NULL,
adrese TEXT NOT NULL,
pilseta TEXT NOT NULL,
abbriviatura TEXT NOT NULL,
indekss INTEGER NOT NULL

);
SELECT * FROM EMPLOYEE WHERE dept = 'Sales';
INSERT INTO EMPLOYEE VALUES (1, 'John Smith', 'jsmith@gmail.com', '123 Main St', 'New York', 'NY', 10001);
INSERT INTO EMPLOYEE VALUES (2, 'Mary Johnson', 'mjohnson@yahoo.com', '456 Oak Ave', 'Los Angeles', 'CA', 90001);
INSERT INTO EMPLOYEE VALUES (3, 'Michael Davis', 'mdavis@hotmail.com','789 Elm St', 'Chicago', 'IL', 60601);
INSERT INTO EMPLOYEE VALUES (4, 'Emily Brown', 'ebrown@gmail.com', '2 Lee', 'dlee@yahoo.com', '567 Maple Ave', 'Miami', 'FL', 33101);
INSERT INTO EMPLOYEE VALUES (6, 'Brian Wilson', 'bwilson@gmail.com','1234 Birch Ave', 'Boston', 'MA', 02101);
INSERT INTO EMPLOYEE VALUES (7, 'Ashley Chen', 'achen@yahoo.com','5678 Oak St', 'San Francisko', 'CA', 94101);
INSERT INTO EMPLOYEE VALUES (8, 'Matthew Park', 'mpark@hotmail.com', '9012 Maple Blvd', 'Dallas', 'TX', 75201);
INSERT INTO EMPLOYEE VALUES (9, 'Je34 Pine St', 'Houston', 'TX', 77001);
INSERT INTO EMPLOYEE VALUES (5, 'Davidsssica Kim', 'jkim@hotmail.com', '890 Cedar St', 'Seattle', 'WA', 98101);
INSERT INTO EMPLOYEE VALUES (10, 'Sarah Thompson', 'sthompson@gmail.com','3456 Elm St', 'Denver', 'CO', 80201);
SELECT * FROM EMPLOYEE;

SELECT * FROM EMPLOYEE WHERE abbriviatura = 'MA';

SELECT COUNT(Id)
FROM EMPLOYEE;
SELECT COUNT(Id)
FROM EMPLOYEE
WHERE abbriviatura = 'TX';

SELECT COUNT(Id)
FROM EMPLOYEE
WHERE abbriviatura = 'WA' AND name = 'Brian Wilson';

SELECT COUNT(Id)
FROM EMPLOYEE
WHERE abbriviatura = 'MA' AND name = 'Jessica Kim';
SELECT name, epasts FROM EMPLOYEE WHERE Id = 3;
SELECT name FROM EMPLOYEE WHERE abbriviatura = 'CA';
UPDATE EMPLOYEE SET pilseta = 'New York' WHERE Id = 8;
UPDATE EMPLOYEE SET pilseta = 'New York' WHERE Id = 4;
UPDATE EMPLOYEE SET name = 'Ashley Chen' WHERE Id = 8;
SELECT * FROM EMPLOYEE;

SELECT pilseta, COUNT(*) as count
FROM EMPLOYEE
GROUP BY pilseta
ORDER BY count desc
LIMIT 1;

SELECT name, COUNT(*) as count
FROM EMPLOYEE
GROUP BY name
ORDER BY count desc

LIMIT 1;
