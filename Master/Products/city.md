# City API Spec

## Get Country API

Method : GET

Parameter : 

Endpoint : /api/master/city

Query : select city_id, city_code 'Kode kota', city_name 'Nama kota', state_name 'Nama propinsi', country_name 'Negara'
, c.created_on 'Tanggal input', c.created_by 'User input', c.updated_on 'Tanggal update', c.updated_by 'User update'
from precise.city c
left join precise.state s on c.state_id = s.state_id
left join precise.country co on s.country_id = co.country_id
;

Response Body :

```json
{
    "status":"ok",
    "data":{[
        "city_id":"",
        "city_code":"",
        "city_name":"",
        "state_name":"",
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

Query : select city_code, city_name, state_id from precise.city where city_id = :city_id;

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
- :type  <!-- code and name ->
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