# gmail-integration
This is to integration gmail via MuleSoft

start here: https://docs.mulesoft.com/email-connector/1.3/email-examples

## Learnings:
1. understanding of email protocols at high level:

  a. SMTP : simple mail transfer protocol
  this is for sending emails.
  
  b. IMAP: Internal message access protocol
  this is to read email  (MuleSoft supports deletion of the read email )
  
  c. POP3 : post office protocol
  this is to read emails and also delete it after retrieval 
  
 2. It is needed to enable "allow low security apps to access" on your gmail settings, for the gmail account which you use for sending email.
  to use simple SMTP, if not go with SMTPS and cofigure TLS. 
   
 3. For reading email ("list" or "On new email" ), keep protocol as IMAPS or POP3S and configure TLS certs.
 for testing purposes, check the "inSecure" button if you do not have certs to configure. 
 
 4. interestingly also learnt that we need to enable properties in connnector seetings, advance tab. 
   
 *mail.smtp.starttls.enable : true*
 
 *mail.imap.starttls.enable : true*
 
![screenShot](https://user-images.githubusercontent.com/49124895/106854876-07474a80-66f7-11eb-8073-aa8ea5375ed7.png)
 
 If true, enables the use of the STARTTLS command (if supported by the server) to switch the connection to a TLS-protected connection before issuing any login commands. If the server does not support STARTTLS, the connection continues without the use of TLS; see the mail.smtp.starttls.required property to fail if STARTTLS isn't supported. Note that an appropriate trust store must configured so that the client will trust the server's certificate. Defaults to false.
 
 check  more on here: https://javaee.github.io/javamail/docs/api/com/sun/mail/smtp/package-summary.html
 
 
 
 Note: change properties.yaml with valid email details.

