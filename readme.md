# jsondb [![Build Status](https://travis-ci.org/gunthercox/jsondb.svg)](https://travis-ci.org/gunthercox/jsondb)

This is a utility for managing content in a database which stores
content in JSON format.

## Usage

```python
from jsondb.db import Database
db = Database("mydata.db")
```

The database has an attribute which works similar to [jQuery's data](http://api.jquery.com/data/) attribute.

```python
# Getting all data
db = Database("mydata.db")
print(db.data())
```

```python
# Getting a stored value
db = Database("mydata.db")
print(db.data(key="user_count"))
```

**It is important to note that a key will be created reguardless of whether it
exists as long as a value is provided.** The database has the same functionality
as a dictionary.

```python
# Setting a value
db = Database("mydata.db")
db.data(key="user_count", value=241)
```

```python
# Passing in a dictionary value
db = Database("mydata.db")
data = {
    "user_id": 234565,
    "user_name": "AwesomeUserName",
    "is_moderator": True
    ""
}
db.data(dictionary=data)
```
