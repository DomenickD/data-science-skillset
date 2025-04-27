# Lesson 5: Data Storage with SQLite3

### Objectives
- Use the built-in `sqlite3` module to persist chat history  
- Design a simple database schema for messages  
- Perform basic CRUD operations in Python

### Prerequisites
- Completion of Lesson 4

### Topics Covered
- Connecting to a SQLite database (`sqlite3.connect`)  
- Creating tables and defining schemas  
- Executing `INSERT`, `SELECT`, `UPDATE`, and `DELETE` statements  
- Committing transactions and handling rollbacks

### In-Class Exercise: Persistent Chat Log
```python
import sqlite3

conn = sqlite3.connect('chatbot.db')
cur = conn.cursor()
# Create table
cur.execute('''
CREATE TABLE IF NOT EXISTS messages (
    id INTEGER PRIMARY KEY,
    user TEXT NOT NULL,
    bot TEXT NOT NULL,
    timestamp DATETIME DEFAULT CURRENT_TIMESTAMP
)''')
conn.commit()
# Insert a chat turn
cur.execute(
    "INSERT INTO messages (user, bot) VALUES (?, ?)",
    ('Hello!', 'Hi there!')
)
conn.commit()
```

### Homework

- Implement functions to retrieve the last N messages

- Add an UPDATE method to edit stored messages

- Handle database migrations by checking schema version