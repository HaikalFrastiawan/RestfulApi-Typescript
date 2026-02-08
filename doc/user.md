# USER API SPEC

## REGISTER USER
End Point : POST /api/users

Respon Body
```json
{
    "username" : "haikal",
    "password" : "rahasia",
    "name" : "ekal"
}
```

Response Body (Success)
```json
{   
    "data" : {
        "username" : "haikal",
        "name" : "ekal"
    }
}
```

Response Body (failed)
```json
{   
    "erorrs" : "username Have not found:"
}
```


## LOGIN USER
End Point : POST /api/users/login

Respon Body
```json
{
    "username" : "haikal",
    "password" : "rahasia",
    "name" : "ekal"
}
```

Response Body (Success)
```json
{   
    "data" : {
        "username" : "haikal",
        "name" : "ekal",
        "token" : "uuid"
    }
}
```

Response Body (failed)
```json
{   
    "erorrs" : "username or password wrong..."
}
```


## GET USER

End Point : GET /api/users/current

 
Response Body (Success)
```json
{   
    "data" : {
        "username" : "haikal",
        "name" : "ekal",
    }
}
```

Response Body (failed)
```json
{   
    "erorrs" : "unauthorize"
}
```

## UPDATE USER
End Point : PATCH /api/users/current

Request Header 
- X-API-TOKEN : token



Request  Body
```json
{
    "password" : "rahasia", //tidak wajib
    "name" : "ekal", // tidak wajib
}
```

Response Body (Success)
```json
{   
    "data" : {
        "username" : "haikal",
        "name" : "ekal",
    }
}
```

Response Body (failed)
```json
{   
    "erorrs" : "unauthorize"
}
```


## LOGOUT USER
End Point : DELETE /api/users/current

Request Header 
- X-API-TOKEN : token



Response Body (Success)
```json
{   
    "data" : "OK"
}
```

Response Body (failed)
```json
{   
    "erorrs" : "unauthorize"
}
```
