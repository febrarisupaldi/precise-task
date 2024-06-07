# City API Spec

## Get Country API

Method : GET

Parameter : 

Endpoint : /api/master/city

Response Body :

```json
{
    "status":"ok",
    "data":{[
        "city_id":"",
        "city_code":"",
        "city_name":"",
        "created_on":"",
        "created_by":"",
        "updated_on":"",
        "updated_by":""
    ]},
    "id":"",
    "message":""
}
```

## List City API

Method : GET

Endpoint : /api/master/city/:idcity

Parameter : :idcity

Response Body :

```json
{
    "status":"ok",
    "data":{[
        "city_id":"",
        "city_code":"",
        "city_name":"",
        "created_on":"",
        "created_by":"",
        "updated_on":"",
        "updated_by":""
    ]},
    "id":"",
    "message":""
}
```

## Create City API

Method : POST

Endpoint : /api/master/city

Request Body :

- city_code
- city_name
- created_by

Response Body :

```json
{
    "status":"ok",
    "message":"success input data",
    "data":{
        "city_code":"",
        "city_name":"",
        "created_by":"",
    },
    "id":""
}
```

## Update City API

Method : PUT

Endpoint: /api/master/city/:idcity

Parameter : :idcity

Request Body :

- city_code
- city_name
- updated_by
- reason

Response Body :

```json
{
    "status":"ok",
    "message":"success update data",
    "data":{
        "city_code":"",
        "city_name":"",
        "created_by":"",
    },
    "id":""
}
```

## Validate Data City API

Method : GET

Endpoint : /api/master/city/check?type=:type&value=:value

Parameter:
- :type <!-- code and name ->
- :value

Response Body :

```json
{
    "status":"ok",
    "message":1,
    "data":{},
    "id":""
}
```