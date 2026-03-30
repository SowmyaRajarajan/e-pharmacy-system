# 🧪 E-Pharmacy Management System (MongoDB)

## 📌 Overview

This project is a **MongoDB-based E-Pharmacy System** designed to manage medicine inventory, patient records, sales transactions, automated billing, and business analytics.

It demonstrates **NoSQL database design, schema validation, CRUD operations, aggregation pipelines, and error handling** in a real-world pharmacy workflow.

---

## 🧩 Modules

### 1️⃣ Inventory Module

* Manages medicine stock, pricing, expiry, and import batches
* Ensures valid data using **schema validation**
* Supports stock updates and expiry-based deletion

---

### 2️⃣ Patient Module

* Stores patient details and loyalty status
* Identifies **regular patients** eligible for discounts
* Enforces strict validation for boolean and discount values

---

### 3️⃣ Sales Module

* Records all medicine transactions
* Tracks quantity sold and total price
* Ensures valid transaction data (no negative or invalid entries)

---

### 4️⃣ Billing Module

* Generates bills dynamically using inventory and patient data
* Applies **automatic 10% discount** for regular patients
* Stores final billing records

---

### 5️⃣ Aggregation Module (Analytics)

* Performs advanced analytics using MongoDB pipelines
* Generates:

  * Units sold per medicine
  * Remaining stock
  * Itemized revenue
  * Total revenue

---

## ⚙️ Features

* ✅ Schema validation using `$jsonSchema`
* ✅ Strict data typing (`decimal`, `int`, `bool`, `date`)
* ✅ Full CRUD operations across modules
* ✅ Automated billing logic
* ✅ Advanced aggregation pipelines
* ✅ Error handling and validation testing

---

## 📊 Sample Aggregation Output

```json
{
  "itemized": [
    {
      "medicine": "Paracetamol",
      "unitsSold": 10,
      "pricePerUnit": 22.0,
      "total": 220.0
    }
  ],
  "grandTotal": [
    {
      "totalRevenue": 220.0
    }
  ]
}
```

---

## 🛡️ Validation & Error Handling

The system prevents invalid data using schema validation and tested error scenarios:

* ❌ Negative price or quantity
* ❌ Incorrect data types
* ❌ Missing required fields
* ❌ Invalid aggregation queries (e.g., wrong operators, missing `_id`)

These validations ensure **data integrity and reliability**.

---

## 🔄 Workflow

```text
Inventory → Sales → Patient → Billing → Aggregation
```

---

## 🧠 Key Concepts Demonstrated

* NoSQL data modeling
* MongoDB schema validation
* Aggregation pipelines (`$lookup`, `$group`, `$facet`)
* Data consistency and error handling
* Real-world business logic implementation

---

## 🚀 Conclusion

This project simulates a **complete pharmacy management system** using MongoDB, showcasing both **operational functionality and analytical capabilities**. It highlights how NoSQL databases can be effectively used in real-world applications.

---
