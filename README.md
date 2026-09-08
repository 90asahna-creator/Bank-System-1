# Bank Management System 🏦

A C++ console-based application designed to manage client records for a banking system. The application uses flat-file storage (`Clients.text`) to persist client data and provides full CRUD (Create, Read, Update, Delete) operations with data validation.

---

## 🚀 Features

* **Show Client List:** View all registered clients formatted in a tabular layout (Account Number, PIN Code, Name, Phone, and Balance).
* **Add New Client:** Add new client profiles with validation to prevent duplicate account numbers.
* **Delete Client:** Remove client records safely using a soft-marking mechanism before persisting changes to the file.
* **Update Client Info:** Search for a client by account number and update their details (PIN, Name, Phone, Balance).
* **Find Client:** Instantly search and view detailed information for any client using their account number.
* **Data Persistence:** All transactions and modifications are saved to a local file (`Clients.text`) using custom string parsing (`#//#` delimiter).

---

## 🛠️ Tech Stack & Concepts Applied

* **Language:** C++
* **File I/O:** `fstream` (`std::ios::in`, `std::ios::out`, `std::ios::app`) for reading and saving data.
* **Data Structures:** `std::vector` for dynamic memory management, Custom `struct` for grouping client attributes.
* **Algorithms & Logic:** Custom string splitting algorithms, Enum-driven menu execution, Search and deletion logic.
* **UI Formatting:** Header libraries like `<iomanip>` for tabular output.

---

## ⚙️ How It Works (Data Storage)

Data is persisted in `Clients.text` using a custom record delimiter `#//#`. 

**Record Format Example:**
```text
A101#//#1234#//#John Doe#//#01000000000#//#5000.000000
A102#//#4321#//#Alice Smith#//#01100000000#//#12500.500000
