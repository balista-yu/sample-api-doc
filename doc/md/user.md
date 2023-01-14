# Group Users

Resources related to users in the API.

## User Collection [/users{?page,limit}]

### List All Users [GET]

+ Parameters
    + page: 1 (number, optional) - page number
    + limit: 10 (number, optional) - limit number
        + Default: 5

+ Response 200 (application/json)
    + Attributes (array[User], fixed-type)

## New User [/users]

### Create a New User [POST]

+ Request (application/json)
    + Attributes (object)
        + name: yamada taro (string, required)
        + age: 35 (number, optional)
        + sex (enum)
            + `men`
            + `women`
            + `unknown` (default)
        + isAdmin: true (boolean, required)

+ Response 201 (application/json)
    + Attributes (object)
        + id: 1 (number)

+ Response 400 (application/json)
    + Attribute (object)
        + message: `Bad Request` (string, required) - error message

## User [/users/{id}]

### View a User Detail [GET]

+ Parameters
    + id: 1 (number)

+ Response 200 (application/json)
    + Attributes (User)

+ Response 404 (application/json)
    + Attribute (object)
        + message: `Not Found` (string, required) - error message

### Update a User [PUT]

+ Parameters
    + id: 1 (number)

+ Request (application/json)
    + Attributes (object)
        + name: yamada taro (string, required)
        + age: 35 (number, optional)
        + sex (enum)
            + `men`
            + `women`
            + `unknown` (default)
        + isAdmin: true (boolean, required)

+ Response 204

+ Response 400 (application/json)
    + Attribute (object)
        + message: `Bad Request` (string)

+ Response 404 (application/json)
    + Attribute (object)
        + message: `Not Found` (string)

### Delete a User [DELETE]

+ Parameters
    + id: 1 (number)

+ Response 204

+ Response 404 (application/json)
    + Attribute (object)
        + message: `Not Found` (string)

# Data Structure

## User (object)
+ id: 1 (number)
+ name: yamada taro (string)
+ age: 40 (number)
+ sex: men (enum)
    + `men`
    + `women`
    + `unknown`
+ isAdmin: true (boolean)
