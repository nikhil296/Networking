# SMTP (Simple mail transfer protocol)  &  POP3:-
- For executing the functionality of email SMTP is used.
- one more protocol named `POP3` is used in combination with SMTP.
- SMTP also uses TCP from transport layer.
- connection for SMTP is setup on port-25.

# How SMTP works ?
- When an email is sent it is sent to the sender's SMTP server using SMTP protocol.
- The SMTP server places the email on a message queue.
- The SMTP server initiates a connection with the receiver's SMTP server and conducts an initial `SMTP handshake`. If the reciever's SMTP server is same as sender's then a seperate coneection is not required.
- Then finally it sends the email to receipients SMTP server.
- The email is downloaded from the receipients SMTP server and then the client shows the mail using the POP3/IMAP server.
- `SMTP          : push protocol (sends the email)`
- `POP/IMAP      : pull protocol (downloads the email)`
- ***Note : If the receipient's SMTP server is offline, the sender SMTP server tries again & again after some delta minutes. There is a set threshold after which it stops sending the email & marks it `not delivered`.***