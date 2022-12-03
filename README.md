Create 3 paths in the swagger.json file.

```
"paths": {
    
}
```

1. swagger.json GET

```
 "/restaurants": {
            "get": {
                "tags": ["Restaurants"],
                "summary": "Get all Restaurants in system",
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "$ref": "#/definitions/Restaurant"
                        }
                    }
                }
            }
        }
```

2. swagger.json POST

```
        "/restaurant": {
            "post": {
                "tags": ["Restaurants"],
                "description": "Create new restaurant in system",
                "parameters": [
                    {
                        "name": "restaurant",
                        "in": "body",
                        "description": "Restaurant that we want to create",
                        "schema": {
                            "$ref": "#/definitions/Restaurant"
                        }
                    }
                ],
                "produces": [
                    "application/json"
                ],
                "responses": {
                    "200": {
                        "description": "New restaurant is created",
                        "schema": {
                            "$ref": "#/definitions/Restaurant"
                        }
                    }
                }
            }
        }
```

3. swagger.json DELETE

```
 "/restaurant/{id}": {
            "parameters": [
                {
                    "name": "id",
                    "in": "path",
                    "required": true,
                    "description": "ID of restaurant that we want to delete",
                    "type": "integer"
                }
            ],
            "delete": {
                "tags": ["Restaurants"],
                "summary": "Delete Restaurant",
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "$ref": "#/definitions/Restaurant"
                        }
                    }
                }
            }
        }
```