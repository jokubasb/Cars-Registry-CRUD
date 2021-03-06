# Car registry

### Launch service
```docker-compose up```

## How to use api

### Test
```curl -v http://localhost/api/v1/```

### Initial Data
```
POST this json into http://localhost/api/v1/ownedcarsArray/ for initial data:

[
    {
        "manufacturer": "Subaru",
        "model": "Impreza",
        "year": 2005,
        "surname": "Bird",
        "name": "Edwin",
        "number": "606-434-2825",
        "email": "EdwinRBird@armyspy.com"
    },
    {
        "manufacturer": "Toyota",
        "model": "Corolla",
        "year": 2010,
        "surname": "Patterson",
        "name": "Sarah",
        "number": "321-512-3924",
        "email": "SarahHPatterson@rhyta.com"
    },
    {
        "manufacturer": "Tesla",
        "model": "Model3",
        "year": 2016,
        "surname": "Hayner",
        "name": "Alisha",
        "number": "678-237-3632",
        "email": "AlishaJHayner@armyspy.com"
    },
    {
        "manufacturer": "Dodge",
        "model": "Challenger",
        "year": 2018,
        "surname": "Moorhead",
        "name": "Amanda",
        "number": "989-397-1216",
        "email": "AmandaCMoorhead@teleworm.us"
    }
]
```

### CREATE:
```
curl -d '{
    "manufacturer": "Ford",
    "model": "Sierra",
    "year": 1995,
    "surname": "Pavardenis",
    "name": "Vardenis",
    "number": "+3706123456",
    "email": "vardeniux@mail.com"
}' -H 'Content-Type: application/json' http://localhost/api/v1/ownedcars/
```
### READ:
(all)
```curl -v http://localhost/api/v1/ownedcars/```

(id)
```curl -v http://localhost/api/v1/ownedcars/1```

### UPDATE:
```curl -d '{
    "manufacturer": "Ford",
    "model": "Sierra",
    "year": 1995,
    "surname": "Pavardenis",
    "name": "Vardenis",
    "number": "+3706123456",
    "email": "vardeniux@mail.com"
}' -H 'Content-Type: application/json' -X PUT http://localhost/api/v1/ownedcars/2```
```
### DELETE:
```curl -X DELETE http://localhost/api/v1/ownedcars/1```
