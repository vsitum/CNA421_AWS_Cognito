# CNA421 AWS_Cognito service 

## Description

This project is for designig, developing and deploying AWS Credentials for Federation Identities with Amazon Cognito. Amazon Cognito let users to sign-up, sign-in, and access control to their web and mobile apps quickly and easily. Amazon Cognito scales to millions of users and supports sign-in with social identity providers, such as Apple, Facebook, Google, and Amazon, and enterprise identity providers via SAML 2.0 and OpenID Connect.

Before we create a social IDP with Amazon Cognito we must register our application with Google to receive a Client ID and a Client Secret. In the Google developer console, we will configure a project. The authorized JavaScript origin we will enter after we have configured our Cognito user Pool. After clicking save Client ID and Client Secret will be created. 

In the Amazon Cognito we will create cognitive user pool and add Amazon Cognito domain. 
In the google console, choose Oauth consent screen in Credentials of our google project, add Amazon Cognito domain. Click on Create Credentials, select OAuth client ID, select Web application from the create credentials list. Now, paste the Amazon Cognito user pool domain into the authorized JavaScript. In The Authorized redirect URLs paste the Amazon Cognito user pool domain, add “/oauth2/idpresponse” to the same URL, and click create. In the Mountly Provider under Federation of Amazon Cognito user pool select Google and enter App Client ID, Client Secret and Profile email open, and click Enable google. Select Google under Attribute mapping and from the list select check box of email, and Email under User pool attribute. Click Save changes. In the App Client settings under App integration enable Google as an IDP by choosing the check Google check box. Enter domain name in the Callback URL(s) and Sign out URL(s), select all check boxes under Allowed OAuth Scopes, and click Save.

## EC2
 Creating AWS EC2 (WooComm-Vlado), installing Bitnami (LEMP), creating Domain name (vladositum.me) in NAmecheap.com and           installingSSL/TLS Certificate(HTTPS)) 

## Google Console:
     1.Create Project to associate one App (user type -external (internal/external organization)), 
     2.Create Credentials (OAuth Client ID(Web App), Client secret, Authorized JavaScript origins (Cognito URL),
 Authorized redirect URL (Cognito URL + oauth2/idpresponse).                                                       
     3.Domain verification (domain, where our app’s running)
   
## Amazon Cognito:
      Create user pool: create app clients (who accesses pool)
                App integration (App client setting (enable identity provider (call back URL,
                                 sign out URL) OAuth2 flows and scope
               Amazon Cognito domain (check availability)
               Federation (Identity providers google, FB, Apple, Login with Amazon.. 
                            attribute mapping email)

