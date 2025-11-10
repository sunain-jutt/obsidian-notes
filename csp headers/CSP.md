a header that controls that which type of data will load on the webpage.

it is sent by backend and frontend to server to control what things should be allowed to load on the webpage.

## important csp headers


| Content-Security-Policy             | Standard modern browsers | main and recommended csp header                                                       |
| ----------------------------------- | ------------------------ | ------------------------------------------------------------------------------------- |
| content-security-policy-report-only | testing mode             | browser reports violations but do not block anything. used to test C before enforcing |
| x-content-security-plocy            | old versions of firefox  | legacy/ outdated                                                                      |
| x-webkit-csp                        | old chrome/ safari       | legacy / outdated                                                                     |

# only 2 matters today
- content-security-policy
- content-security-policy-report-only

## csp directives

|Directive|Controls|Example|Meaning|
|---|---|---|---|
|**default-src**|Default content rule|`default-src 'self'`|Load everything only from same origin|
|**script-src**|JavaScript|`script-src 'self' https://cdn.js.com`|Allow JS only from trusted locations|
|**style-src**|CSS|`style-src 'self' 'unsafe-inline'`|Allow CSS, may allow inline styles|
|**img-src**|Images|`img-src *`|Allow loading images from anywhere|
|**font-src**|Fonts|`font-src https://fonts.googleapis.com`|Control font sources|
|**connect-src**|API Requests / AJAX|`connect-src api.example.com`|Restrict fetch(), XHR calls|
|**frame-src**|iFrames|`frame-src youtube.com`|Allow embedding specific domains|
|**object-src**|Flash, applets|`object-src 'none'`|Block legacy plugin content|
|**report-uri** / **report-to**|Logging violations|`report-uri /csp-violation`|Server receives CSP violation logs|