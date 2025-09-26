#   Exercise 1:

### 1 What kind of authentication is used in the PPP protocol?
- PAP (Password Authentication Protocol)

![img.png](Images/Pergunta1-Protocolo.png)

### 2  What are the steps for authenticating the user?
- PPP connection establishment (LCP Configuration Request/Ack). 
- PAP Authenticate-Request sent (with username and password).
- PAP Authenticate-Ack sent (authentication successful).
- Network layer (IPCP) configuration proceeds.

![img_2.png](Images/Pergunta2-PassosParaAuth.png)

### 3 Identify the ”secret” password.
- The secret password is "aliceadsl"

![img_1.png](Images/Pergunta3-Password.png)

### 4 Imagine you are a telecom provider and you provide this authentication method to your clients, what are your security considerations?
- PAP sends the password in plaintext, making it vulnerable to interception and eavesdropping.
- For that, it is susceptible to replay attacks, where an attacker can capture and reuse authentication messages.
