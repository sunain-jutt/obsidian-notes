

- **Look for inputs that accept URLs or hostnames** used by the server to make backend HTTP requests — common in features like URL fetchers, preview generators, or API proxies.
- **Test by submitting URLs pointing to internal IPs or localhost addresses** (e.g., `http://127.0.0.1`, `http://192.168.x.x`) and see if the server makes requests to those addresses, often by monitoring server responses, errors, or using a collaborator tool to detect outbound requests.
- **Check if the server follows redirects automatically**, which could allow bypassing domain filters through open redirects.
- **Use out-of-band techniques**, like Burp Collaborator or a controlled server, to detect if the target system makes any outbound HTTP/DNS requests in response to user input.
- **Review application logs or network traffic**, if available, to spot unexpected outbound requests to internal or attacker-controlled hosts.