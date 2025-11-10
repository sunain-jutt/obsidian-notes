for example you are on a website and buying something. the product has an id of 1. so the GET request will look like this 
```
GET /api/products/1/price HTTP/2
Host: 0ab9008e03a8267a819b0cbe006000b6.web-security-academy.net
Cookie: session=rlk8nURS17xrdGgFkq88Sgzy3dxlg3NM
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:128.0) Gecko/20100101 Firefox/128.0
Accept: */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: https://0ab9008e03a8267a819b0cbe006000b6.web-security-academy.net/product?productId=1
Sec-Fetch-Dest: empty
Sec-Fetch-Mode: cors
Sec-Fetch-Site: same-origin
Priority: u=4
Te: trailers
```

try to change the request type **GET** to **POST**.  maybe it will provide you some errors that only these request methods are allowed.
use **PATCH**.
after that the response the error may comes up and say 
```
content-type is missing or application/json only applicable
```
 so add this in the request header and in the object make the price of product to 0 and buy it.
