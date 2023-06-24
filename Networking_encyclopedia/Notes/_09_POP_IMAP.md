# POP (post office protocol) :-
- The latest version is POP3.
- It downloads the email in 4 phases.
    1. `Connect`        : user agent will connect to the POP3 server over TCP.
    2. `Authorise`      : user agent authenticates the user using the username and password, to check if the client trying to download the email is correct.
    3. `Transaction`    : after coneection is setup and authentication is done the transaction happens, and the email starts downloading.
    4. `Update`         : user agent quits, POP3 session is closed and the server marks updates on all the emails that are already delivered. Here if the user marks a email to be deleted then the email is deleted from the POP3 server also.
- There are 2 modes of POP :-
    1. Download and keep.
    2. Download and delete.

# IMAP (Internet message access protocol) :-
- Emails are kept on the server and not deleted.
- Local copies of the emails are cached on each device.
- If an email is deleted by user manually then only it gets deleted from server.