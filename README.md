# Flask SQLAlchemy

This is a Flask-based application that demonstrates how to manage a book database using SQLAlchemy ORM. It supports operations such as creating a database, adding initial data, and querying stored records using Flask CLI commands.

---

## **Features**
- Database models for books, authors, publishers, and readers.
- Many-to-many relationships between books, authors, and readers.
- CLI commands to initialize the database, populate data, and query the database.

---

## **Installation and Setup**

### **1. Clone the Repository:**
```bash
# Clone this repository
git clone https://github.com/your-repository/flask-book-management.git
cd flask-book-management
```

### **2. Create a Virtual Environment (Optional):**
```bash
python -m venv venv
source venv/bin/activate  # On Linux/Mac
venv\Scripts\activate   # On Windows
```

### **3. Install Dependencies:**
```bash
pip install Flask Flask-SQLAlchemy
```

### **4. Save the Code:**
- Ensure the application code is saved as `app.py`.

---

## **Running the Application**

### **1. Initialize the Database:**
```bash
export FLASK_APP=app.py

flask initdb
```

### **2. Populate Initial Data:**
```bash
flask bootstrap
```

### **3. Query the Database:**
```bash
flask query
```

---

## **How It Works**

### **Database Models:**
- **Author:** Defines authors with many-to-many relationships with books.
- **Book:** Stores book details, linking to publishers.
- **Publisher:** Contains publisher information and books they publish.
- **Reader:** Tracks readers and books they read.

### **Command-Line Commands:**
1. **initdb:** Initializes the database.
2. **bootstrap:** Populates the database with sample data.
3. **query:** Queries specific authors and their books, including publishers and readers.

---

## **Example Output:**
```text
Initialized default DB.
Added data to DB.
'John Carson' has written 'Intro to Python' published by 'Penguin Random House', read by 'Lily'.
'John Carson' has written 'Intro to Python' published by 'Penguin Random House', read by 'Sam'.
'John Carson' has written 'Intro to C++' published by 'Harper Collins', read by 'Lily'.
```

---

## **Technologies Used**
- Python 3.x
- Flask
- Flask-SQLAlchemy
- SQLite (for data storage)