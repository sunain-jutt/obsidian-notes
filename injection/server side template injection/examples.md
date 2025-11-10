## greeting website
for example there is a website that receive a string as a name and gives an output like "welcome {{name}}".
the html code for the output side is 
```
@app.route("/greeting/<name>")
def greeting(name):
greeting_text = choice(["Hi", "Hello", "Welcome"])
template = '''
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Greeting</title>
<link rel="stylesheet" type="text/css" href="{{ url_for('static', filename='style.css') }}">
</head>
<body>
<div class="greeting-container">
<h1>''' + greeting_text + ' ' + name + '''!</h1>
<p>Thank you for visiting our website!</p>
<a href="/">Go Back</a>
</div>
</body>
</html>'''
return render_template_string(template)
```

see that variable: name is being concatenated before rendering. means it is not plain text.
GET request.
```
GET /greeting/sunain HTTP/1.1
Host: 172.17.0.2:8050
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:140.0) Gecko/20100101 Firefox/140.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: http://172.17.0.2:8050/
Connection: keep-alive
Upgrade-Insecure-Requests: 1
Priority: u=0, i
```

sunain is being stored in name. change sunain to "{{7*7}}" like this 
```
GET /greeting/{{7*7}} HTTP/1.1
Host: 172.17.0.2:8050
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:140.0) Gecko/20100101 Firefox/140.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: http://172.17.0.2:8050/
Connection: keep-alive
Upgrade-Insecure-Requests: 1
Priority: u=0, i
```

it website displays 49 than SSTI is there.