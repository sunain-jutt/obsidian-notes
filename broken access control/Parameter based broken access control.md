their are some parameters that declares the function is being done by the specific logged in person. for example admin=true, id=james.

 If request was sent by the user to server for logging in, thier could be setting cookies option like this
 
 `Cookie: session=KBGFGaQFJhZdREZU4WB5MwgT0v7gHFgy; Admin=false`

  if an attacker intercept this and send this request to server by modifying **Admin=true** he could gain administrative access.