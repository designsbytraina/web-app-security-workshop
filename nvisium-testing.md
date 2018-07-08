github.com/nvisium/djangonv
[http://104.236.151.240:8000/]

REGISTRATION
unable to submit form successfully while including script tags

LOGIN
unable to login if injection in form

csrf token in request
passes username/pw in post request

PROFILE
able to update user profile with scripting in form fields

CHANGE PASSWORD
problems that can occur, sql injection or command injection to update or drop db tables
do they check if correct current password is entered in old password field?

http://104.236.151.240:8000/taskManager/profile/13

Able to see other people's profiles easily
drops you into a django debugging tool so we can see the paths
no httponly flag on the cookie, insecure direct object reference on profiles
leaking usernames makes using a craker tool super simple
we can update info for any user with this method, as well

[<img alt=<script>alert(document.cookie);</script>>]

ADMIN ACCOUNT
goal - create admin account or compromise one
"privilege escalation"
horizontal compromise a low priv user account and use to escalate up

user.id = identifier for user account
user id = 1
username = admin

REGISTER + BENEFITS OF SUPERUSER
is_superuser flag on login successfully submits form
i can now create projects
i can now create tasks
i can now upload files

SECURITY MISCONFIGURATION
able to see all paths if i just request invalid path like:
http://104.236.151.240:8000/taskManager/download_

(select password from auth_user where username='admin'),8);--