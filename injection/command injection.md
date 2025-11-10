how to identify?
	look for the evidence that website is running the OS level command execution in the server.
# enumeration
if there is an input field which is taking IP address from the user to check that the specific ip is available in the local network or live network. (website is for checking ping able ips).
at the backend the website is running the following command:
```
ping [user entered ip]
```

directly enter an OS level command to check the vulnerability.
```
192.168.1.1' ls
```

first ip is to pass the input field for website. ' to end the input field. **ls** to check, if in the output of the website after the ping result if some directories are listing *result by ls*. that means command injection is there.

instead of ls use the desired command.

