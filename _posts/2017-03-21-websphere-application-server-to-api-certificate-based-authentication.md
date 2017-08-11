---
layout: post
title:  "WebSphere Application Server to API certificate based authentication"
date:   2017-03-21 16:16:01 -0600
categories: Application Server, Middleware, Server Admin, WebSphere
---

##WebSphere Application Server to API certificate based authentication

There are times, you wanted to authenticate to APIs from your application using SSL Certificate. 

Below the steps to achieve the same when you are using WebSphere as application server.

1. Logon to WebSphere Admin console. Under the Security select “SSL Certificate and Keystore management”
2. From the Right navigation, click on “Keystores and Certificates” link
3. From the list of Keystores and Trust stores, click on “Node Default Keystore”
4. Select “Personal certificates” from the right navigation
5. Click on import button, and give the certificate information 
  * Select Key store file option
  * Enter the location of the client certificate with the file name
  * Type the password and click on “Get Key File Aliases”
  * Select the Certificate alias to import
  * Type user friendly alias name in Import Certificate alias and
6. Click on OK and save the configuration
7. Under the “Out bond” expand the “Nodes” and select the AppServer node
8. Under the Certificate alias select the Alias which is given to import the client certificate to keystore.
9. Click on OK and save the configurations.
10. Restart the app server.
