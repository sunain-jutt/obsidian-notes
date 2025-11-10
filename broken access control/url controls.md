
in some cases POST method to /admin/deleteuser are restricted to users. like

```
   DENY: POST, /admin/deleteuser/
```

   in this case POST method is restricted to that deleteuser request.


   attackers can use some http headers to by pass this control like this.

```
   X-OIGINAL-URL: /admin/deleteuser

   X-REQRITE-URL: /admin/deleteuser
```


   this in the http headers can re-write the control.
   