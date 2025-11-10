Broken Access is a logical error in which user can perform function that they are not supposed to perform.

# Vertical Access Control
different type of users have access to different type of functions. for examples the admin have to access to almost all the functions like delete or add the users while a normal employee only have access to specific functions.

# horizontal access control
in this access control acccess to resources are restricted to users. for examples a user can only see transactions of his own account using his banking app and credentials, can't see the transaction of others.

## differ between vertical and horizontal

- in vertical high level user and low level users authorities are being restricted

- in horizontal those functions are restricted to others which belongs to a specific user.
## context dependant access control

this prevent the user to modify some restricted data based on user-interaction or state of the website. for example if a user add a product in the shoping cart after that he might not be able to modify the data after this.

## url matching functions

in some websites devalopers add the **usesuffixPatternMatch** function in the code. it means that /admin/deleteuser.something will do the same thing as /admin/deleteuser.

## Examples for broken access controls.

- in the url example.com/robots.txt robots.txt should not be accessable by everyone.

  because hackers can do a brute force on directory of a website's url and can find important urls.

- urls like examples.com/admin-mpv45 is not easily guessable. many times this could be found in

  in the JS section or under the script tags in html