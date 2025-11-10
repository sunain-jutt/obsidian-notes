if robots.txt is accessable try to access the Allowed urls.

## security by obscurity

lets say their is a url admin-panel-6457 which is not that easily guessable by hackers. so theri can be chances that their is a code of it in javascript of website like this.

```
`var isAdmin = false;`

    `if (isAdmin) {`

        `...`

        `var adminPanelTag = document.createElement('a');`

        `adminPanelTag.setAttribute('href', 'https://insecure-website.com/administrator-panel-yb556');`

        `adminPanelTag.innerText = 'Admin panel';`

        `...`

    `}`
```

## parameters

   **Cookie: session=KBGFGaQFJhZdREZU4WB5MwgT0v7gHFgy; Admin=false**

   attacker could intercept and modify **Admin=true**
