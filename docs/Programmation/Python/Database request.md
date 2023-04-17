

#### Postgresql/MySQL

```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="root",
  password="root",
  database="db_test"
)

mycursor = mydb.cursor()

mycursor.execute("SELECT * FROM [nom_table]")

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```

---

#### SQLite3

```python
def create_connection(db_file):
    """ create a database connection to a SQLite database """
    conn = None
    try:
        conn = sqlite3.connect(db_file)
    except Error as e:
        print(e)
    finally:
        if conn:
            conn.close()
```