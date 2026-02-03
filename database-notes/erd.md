# /database-notes/erd.md notes: 

## What is ERD?
ERD (Entity Relationship Diagram) is a simple diagram that helps me plan the database by showing the main tables and how they connect.

## Components 
**Entity**: a table (example: Book, Member)
**Attribute**: a column inside the table (example: title, name)
**PK (Primary Key)**: unique ID for each record (example: book_id)
**FK (Foreign Key)**: a field that links to another table’s PK (example: member_id in Loan)

## Relationships (With quick examples)
**1–1**: one thing matches one thing (Person ↔ Passport)
**1–M**: one matches many (Customer → Orders)
**M–M**: many matches many (Students ↔ Courses) → needs a middle table (Enrollment)

## Mini Library ERD (Example)
Tables:
**Book**(book_id PK, title, author, is_available)
**Member**(member_id PK, name)
**Loan**(loan_id PK, member_id FK, book_id FK, date)

Relationships:
**Member 1–M Loan**
**Book 1–M Loan**

## Diagram
I will upload the ERD image to /diagrams/ and reference it here.

## ERD Diagram
![Library ERD](/diagrams/library-erd..png)
<img width="512" height="427" alt="image" src="https://github.com/user-attachments/assets/f18b25b0-89de-4762-9e5d-923d05669ed7" />
