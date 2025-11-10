Sending parallel requests with different values to a single endpoint can sometimes trigger powerful race conditions.
Consider a password reset mechanism that stores the user ID and reset token in the user's session.
In this scenario, sending two parallel password reset requests from the same session, but with two different usernames, could potentially cause the following collision:

![[Pasted image 20251110063302.png]]

Note the final state when all operations are complete:
- `session['reset-user'] = victim`
- `session['reset-token'] = 1234`