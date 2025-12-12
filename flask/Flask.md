- [Flask REST API](#flask-rest-api)
  - [First REST API](#first-rest-api)
- [Flask CLI](#flask-cli)
  - [flask run](#flask-run)

# Flask REST API

## First REST API

```
from flask import Flask

app = Flask(__name__)

stores = [{"name": "My Store", "items": [{"name": "my item", "price": 15.99}]}]

@app.get("/store")
def get_stores():
    return {"stores": stores}
```

# Flask CLI

## flask run

- Run web application
