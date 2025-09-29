Perfect 🚀 You gave me your **SQL table definition + data**, now I’ll show you how it looks in **MongoDB**.

---

## SQL Table (CUSTOMERS)

```sql
CREATE TABLE CUSTOMERS(
  ID INT NOT NULL,
  NAME VARCHAR(20) NOT NULL,
  AGE INT NOT NULL,
  ADDRESS CHAR(25),
  SALARY DECIMAL(18, 2),
  PRIMARY KEY (ID)
);
```

### Inserted Data:

| ID | NAME     | AGE | ADDRESS   | SALARY  |
| -- | -------- | --- | --------- | ------- |
| 1  | Ramesh   | 32  | Ahmedabad | 2000.00 |
| 2  | Khilan   | 25  | Delhi     | 1500.00 |
| 3  | Kaushik  | 23  | Kota      | 2000.00 |
| 4  | Chaitali | 25  | Mumbai    | 6500.00 |
| 5  | Hardik   | 27  | Bhopal    | 8500.00 |
| 6  | Komal    | 22  | MP        | 4500.00 |

---

## MongoDB Equivalent (Collection: `customers`)

Each **row** → becomes a **document**.
SQL **Primary Key (ID)** → MongoDB’s `_id`.

```json
{
  "_id": 1,
  "name": "Ramesh",
  "age": 32,
  "address": "Ahmedabad",
  "salary": 2000.00
}
```

```json
{
  "_id": 2,
  "name": "Khilan",
  "age": 25,
  "address": "Delhi",
  "salary": 1500.00
}
```

```json
{
  "_id": 3,
  "name": "Kaushik",
  "age": 23,
  "address": "Kota",
  "salary": 2000.00
}
```

```json
{
  "_id": 4,
  "name": "Chaitali",
  "age": 25,
  "address": "Mumbai",
  "salary": 6500.00
}
```

```json
{
  "_id": 5,
  "name": "Hardik",
  "age": 27,
  "address": "Bhopal",
  "salary": 8500.00
}
```

```json
{
  "_id": 6,
  "name": "Komal",
  "age": 22,
  "address": "MP",
  "salary": 4500.00
}
```

---

## MongoDB Insert Command

Instead of SQL `INSERT`, you use `insertMany()` in MongoDB:

```javascript
db.customers.insertMany([
  { _id: 1, name: "Ramesh", age: 32, address: "Ahmedabad", salary: 2000.00 },
  { _id: 2, name: "Khilan", age: 25, address: "Delhi", salary: 1500.00 },
  { _id: 3, name: "Kaushik", age: 23, address: "Kota", salary: 2000.00 },
  { _id: 4, name: "Chaitali", age: 25, address: "Mumbai", salary: 6500.00 },
  { _id: 5, name: "Hardik", age: 27, address: "Bhopal", salary: 8500.00 },
  { _id: 6, name: "Komal", age: 22, address: "MP", salary: 4500.00 }
]);
```

---

✅ That’s your SQL → MongoDB conversion.

Do you also want me to **write a Python script** that reads from SQL and directly inserts into MongoDB automatically?
