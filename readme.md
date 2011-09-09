Passkey
=======

*Copyright 2011, Adam Kalsey http://kalsey.com/*

External authentication for Drupal. Integrate Drupal with your corporate intranet, an 
LDAP database, or use Facebook or some other login provider to log into your site.

Passkey provides a framework for authenticating users into Drupal using something other 
than Drupal's user table. The module passes the user's username and password to your code 
and you return true or false. It's that simple.

The code can be another module (there's a hook provided: hook_passkey_auth) or a PHP 
snippet entered into the admin settings.

All authenticated users end up as real Drupal users, so modules that work with users 
will work just fine. Roles, node authorship, and anything else. You can even pick a role 
and auto-assign users who log in with the external system to that role.

For now, Passkey assumes the external authentication is the only user database -- you 
can't mix and match Drupal and external users.

Planned enhancements:
---------------------

* Namespace external users, allowing local and external auth to mix
* cleaner integration of user management functions
* allow the external system to return data about the user
