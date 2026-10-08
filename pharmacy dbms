CREATE DATABASE Pharmacy;
USE Pharmacy;
CREATE TABLE Tablets (
    Tablet_ID INT PRIMARY KEY,
    Tablet_Name VARCHAR(100),
    Tablet_Weight DECIMAL(6,2),
    Disease VARCHAR(100),
    Symptom VARCHAR(100)
);
ALTER TABLE Tablets
ADD Cost DECIMAL(10,2);
ALTER TABLE Tablets
RENAME COLUMN Cost TO Tablet_Cost;
INSERT INTO Tablets
(Tablet_ID, Tablet_Name, Tablet_Weight, Disease, Symptom, Tablet_Cost)
VALUES
(1, 'Paracetamol', 500.00, 'Fever', 'Headache', 20.00),
(2, 'Amoxicillin', 250.00, 'Infection', 'Sore Throat', 50.00),
(3, 'Cetirizine', 10.00, 'Allergy', 'Sneezing', 15.00),
(4, 'Ibuprofen', 400.00, 'Pain', 'Body Pain', 30.00),
(5, 'Azithromycin', 500.00, 'Infection', 'Fever', 80.00),
(6, 'Aspirin', 300.00, 'Heart Disease', 'Chest Pain', 25.00),
(7, 'Metformin', 500.00, 'Diabetes', 'High Sugar', 40.00),
(8, 'Omeprazole', 20.00, 'Acidity', 'Heartburn', 35.00),
(9, 'Loratadine', 10.00, 'Allergy', 'Runny Nose', 25.00),
(10, 'Diclofenac', 50.00, 'Pain', 'Joint Pain', 45.00),
(11, 'Pantoprazole', 40.00, 'Acidity', 'Stomach Pain', 30.00),
(12, 'Doxycycline', 100.00, 'Infection', 'Cough', 60.00),
(13, 'Losartan', 50.00, 'Blood Pressure', 'Dizziness', 55.00),
(14, 'Montelukast', 10.00, 'Asthma', 'Breathing Problem', 70.00),
(15, 'Glimepiride', 2.00, 'Diabetes', 'Weakness', 35.00),
(16, 'Naproxen', 250.00, 'Pain', 'Back Pain', 40.00),
(17, 'Ranitidine', 150.00, 'Acidity', 'Indigestion', 20.00),
(18, 'Levocetirizine', 5.00, 'Allergy', 'Itching', 30.00),
(19, 'Clopidogrel', 75.00, 'Heart Disease', 'Chest Pain', 90.00),
(20, 'Salbutamol', 4.00, 'Asthma', 'Breathing Problem', 65.00);
UPDATE Tablets
SET Tablet_Cost = 25.00
WHERE Tablet_ID = 1;
UPDATE Tablets
SET Tablet_Cost = 55.00
WHERE Tablet_ID = 2;
UPDATE Tablets
SET Tablet_Cost = 18.00
WHERE Tablet_ID = 3;
ALTER TABLE Tablets
DROP COLUMN Disease;
ALTER TABLE Tablets
ADD Age INT;
UPDATE Tablets
SET Age = 18
WHERE Tablet_ID IN (1, 3, 4, 9);
UPDATE Tablets
SET Age = 30
WHERE Tablet_ID IN (2, 5, 6, 7, 8);
UPDATE Tablets
SET Age = 45
WHERE Tablet_ID IN (10, 11, 12, 13, 14);
UPDATE Tablets
SET Age = 60
WHERE Tablet_ID IN (15, 16, 17, 18, 19, 20);
SELECT Age, COUNT(*) AS Tablet_Count
FROM Tablets
GROUP BY Age
HAVING Age >= 30;
SELECT Symptom, COUNT(*) AS Number_Of_Tablets
FROM Tablets
GROUP BY Symptom;
SELECT * FROM Tablets;
SELECT MIN(Tablet_Weight) AS Minimum_Weight
FROM Tablets;
SELECT MAX(Tablet_Weight) AS Maximum_Weight
FROM Tablets;
ALTER TABLE Tablets
ADD Qty INT;
UPDATE Tablets SET Qty = 10 WHERE Tablet_ID = 1;
UPDATE Tablets SET Qty = 15 WHERE Tablet_ID = 2;
UPDATE Tablets SET Qty = 20 WHERE Tablet_ID = 3;
UPDATE Tablets SET Qty = 12 WHERE Tablet_ID = 4;
UPDATE Tablets SET Qty = 8 WHERE Tablet_ID = 5;
UPDATE Tablets SET Qty = 10 WHERE Tablet_ID = 6;
UPDATE Tablets SET Qty = 25 WHERE Tablet_ID = 7;
UPDATE Tablets SET Qty = 15 WHERE Tablet_ID = 8;
UPDATE Tablets SET Qty = 20 WHERE Tablet_ID = 9;
UPDATE Tablets SET Qty = 10 WHERE Tablet_ID = 10;
UPDATE Tablets SET Qty = 18 WHERE Tablet_ID = 11;
UPDATE Tablets SET Qty = 12 WHERE Tablet_ID = 12;
UPDATE Tablets SET Qty = 10 WHERE Tablet_ID = 13;
UPDATE Tablets SET Qty = 15 WHERE Tablet_ID = 14;
UPDATE Tablets SET Qty = 20 WHERE Tablet_ID = 15;
UPDATE Tablets SET Qty = 10 WHERE Tablet_ID = 16;
UPDATE Tablets SET Qty = 15 WHERE Tablet_ID = 17;
UPDATE Tablets SET Qty = 25 WHERE Tablet_ID = 18;
UPDATE Tablets SET Qty = 8 WHERE Tablet_ID = 19;
UPDATE Tablets SET Qty = 20 WHERE Tablet_ID = 20;
SELECT
    Tablet_ID,
    Tablet_Name,
    Tablet_Weight * Qty AS Total_Weight,
    Symptom
FROM Tablets;
SELECT
    Tablet_ID,
    Tablet_Name,
    Tablet_Weight,
    Symptom
FROM Tablets
WHERE Tablet_Weight >= 100
AND Age >= 30;
