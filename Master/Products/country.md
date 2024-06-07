# Country API Spec

## Get Country API

Method : GET

Parameter : 

Endpoint : /api/master/country

Response Body :

```json
{
    "status":"ok",
    "data":{[
        "country_id":"",
        "country_code":"",
        "country_name":"",
        "created_on":"",
        "created_by":"",
        "updated_on":"",
        "updated_by":""
    ]},
    "id":"",
    "message":""
}
```

## List Country API

Method : GET

Endpoint : /api/master/country/:idcountry

Parameter : :idcountry

Response Body :

```json
{
    "status":"ok",
    "data":{[
        "country_id":"",
        "country_code":"",
        "country_name":"",
        "created_on":"",
        "created_by":"",
        "updated_on":"",
        "updated_by":""
    ]},
    "id":"",
    "message":""
}
```

## Create Country API

Method : POST

Endpoint : /api/master/country

Request Body :

- country_code
- country_name
- created_by

Response Body :

```json
{
    "status":"ok",
    "message":"success input data",
    "data":{
        "country_code":"",
        "country_name":"",
        "created_by":"",
    },
    "id":""
}
```

## Update Country API

Method : PUT

Endpoint: /api/master/country/:idcountry

Parameter : :idcountry

Request Body :

- country_code
- country_name
- updated_by
- reason

Response Body :

```json
{
    "status":"ok",
    "message":"success update data",
    "data":{
        "country_code":"",
        "country_name":"",
        "created_by":"",
    },
    "id":""
}
```

## Validate Data Country API

Method : GET

Endpoint : /api/master/country/check?type=:type&value=:value

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