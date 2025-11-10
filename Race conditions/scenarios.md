- rate limit
- coupon code that must be add only one time
- adding one more thing in the in the cart before checking out. while during the payment validation add more objects into the cart.
- hidden multi step sequences, for example:

```
session['userid'] = user.userid 
if user.mfa_enabled: session['enforce_mfa'] = True 
# generate and send MFA code to user 
# redirect browser to MFA code entry form
```
As you can see, this is in fact a multi-step sequence within the span of a single request.

Most importantly, it transitions through a sub-state in which the user temporarily has a valid logged-in session, but MFA isn't yet being enforced. An attacker could potentially exploit this by sending a login request along with a request to a sensitive, authenticated endpoint.






