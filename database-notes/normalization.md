# normalization notes:

## What is normalization?
Normalization is organizing database tables by splitting data into smaller tables so the same info doesn’t repeat.

## Why do we use it?
Reduce duplicate data (less repetition)
Make updates easier (change once, not many times)
Avoid data problems (update/delete/insert issues)
Keep data clean and consistent

## 1NF / 2NF / 3NF (quick)
**1NF** : Each field should store one value only (no lists in one cell).
**2NF** : If the PK is composite (2+ columns), other columns must depend on the whole key, not part of it.
**3NF** : Non-key columns shouldn’t depend on other non-key columns (move that info to a separate table).

## Before / After (example)
**Before (not normalized)**
Orders(order_id, customer_name, customer_phone, product_name)
**After (normalized)**
Customer(customer_id PK, name, phone)
Product(product_id PK, name)
Orders(order_id PK, customer_id FK, product_id FK)

## Anomalies (problems)
Insert anomaly: I can’t add data without adding another related row.
Update anomaly: Same info repeats, so updating it in one place may leave other rows wrong.
Delete anomaly: Deleting a row can accidentally remov
