# `Nikhil_Auth` :-
1. work account will send a request to browser to get authenticated by SSO.
2. browser will send a request to `Nikhil_Auth` SSO service provider.
3. `Nikhil_Auth` will send back a sign_in page to browser, to just enter your work email.
4. The browser will send the request to `Nikhil_Auth` SSO with email entered.
5. The `Nikhil_Auth` SSO will send a notification on your mobile device, to login to the mobile authenticator application.
6. Login is done using the mobile device's native login credentials, may it be FINGERPRINT or PASSCODE, etc.
7. after Login is done, the User is asked to draw the `PATTERN` on the drawing board of the Mobile app.
8. The `PATTERN` is the agreed pattern while signing up for the `Nikhil_Auth` SSO service provider. this also need to be updated by the user on agreed upon frequency, ie. Weekly, Monthly, Annual, etc.
9. Once the pattern is validated, the request is sent to `Nikhil_Auth` SSO with validation request.
10. `Nikhil_Auth` SSO hen validates the user and sends a `SAML` certificate to the browser, which the browser in turn sends it back to the Work account of the app we are trying to login.
11. The login process is thus complete.
12. The work app will have some sort of mechanism to validate the certificate with `Nikhil_Auth` SSO like an agreed upon Private Key, etc.