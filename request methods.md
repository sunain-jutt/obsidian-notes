
| GET     | retreive data                                |
| ------- | -------------------------------------------- |
| POST    | create data                                  |
| DELETE  | delete data                                  |
| PATCH   | modify data                                  |
| OPTIONS | retrive information about the request method |

## Curl usage 

get request 

```
curl <ip or domain>
```

get request with parameters

```
curl <ip or domain>/example.php?<param>=<value>
```

POST request

```
curl -X POST <ip or domain>
```

POST with parameters

```
curl -X POST -d "param=value" <ip or domain>/example.php
```

