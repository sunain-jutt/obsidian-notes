this happens when client-side inputs embed into the server-side request to the internal API.
this could lead the client to inject something malicious that could directly hit the server or APIs. client can control the whole server and requests.

### server-side parameter pollution in REST paths

Consider an application that enables you to edit user profiles based on their username. Requests are sent to the following endpoint:
```
GET /edit_profile.php?name=peter
```
This results in the following server-side request:
```
GET /api/private/users/peter
```
You could submit URL-encoded `peter/../admin` as the value of the `name` parameter:
```
GET /edit_profile.php?name=peter%2f..%2fadmin
```
This may result in the following server-side request:
```
GET /api/private/users/peter/../admin
```
