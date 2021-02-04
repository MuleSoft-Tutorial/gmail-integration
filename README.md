# gmail-integration
This is to integration gmail via MuleSoft

# Learnings:
1. understandig of email protocols at high level:

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
  
 mail.smtp.starttls.enable : true
 mail.imap.starttls.enable : true
 
 

