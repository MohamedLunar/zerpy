# ZerPy
- **ZerPy** is a poweful database and environment managing you can found it on [PyPI](https://pypi.org/project/zerpy)
# Package Guide
## #1 Installation
- You can install **ZerPy** package via:
```bash
pip install zerpy
```
## #2 Usage
- Connect & Registring & Load databases
```python
import zerpyimport zerpy
from zerpy import db

# Connect to a database
db = zerpy.connect("example.db")

# Load data from the database
db.load()

# Retrieve data from a specific database
USER_ID = db.get_database("USER")
print(USER_ID)

# Register new data into the database
db.register(USER_ID = "12345", USERNAME = "user_example")

# Delete specific data
db.delete("USER_ID")
```
- Managing .env
```python
import zerpyimport zerpy
from zerpy import env
import os

# Load environment variables from .env file
env.load()

# Get the value of environment variables
API_KEY = os.getenv("API_KEY")
print(API_KEY)
```
