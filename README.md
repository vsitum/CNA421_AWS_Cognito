# CNA421_AWS_Cognito

The Galaxy will design and develop and deploy AWS Credentials for Federation Identities with Amazon Cognito. Amazon Cognito let users to sign-up, sign-in, and access control to their web and mobile apps quickly and easily. Amazon Cognito scales to millions of users and supports sign-in with social identity providers, such as Apple, Facebook, Google, and Amazon, and enterprise identity providers via SAML 2.0 and OpenID Connect.

Before we create a social IDP with Amazon Cognito we must register our application with Google to receive a Client ID and a Client Secret. In the Google developer console, we will configure a project. The authorized JavaScript origin we will enter after we have configured our Cognito user Pool. We will see Client ID and Client Secret. 

In the Amazon Cognito we will create cognitive user pool and add Amazon Cognito domain. 
In the google console, choose Oauth consent screen in Credentials of our google project, add Amazon Cognito domain. Click on Create Credentials, select OAuth client ID, select Web application from the create credentials list. Now, paste the Amazon Cognito user pool domain into the authorized JavaScript. In The Authorized redirect URLs paste the Amazon Cognito user pool domain, add “/oauth2/idpresponse” to the same URL, and click create. After this creation we will see Client ID and Client secret. In the Mountly Provider under Federation of Amazon Cognito user pool select Google and enter App Client ID, Client Secret and Profile email open, and click Enable google. Select Google under Attribute mapping and from the list select check box of email, and Email under User pool attribute. Click Save changes. In the App Client settings under App integration enable Google as an IDP by choosing the check Google check box. Enter domain name in the Callback URL(s) and Sign out URL(s), select all check boxes under Allowed OAuth Scopes, and click Save.

The Galaxy LLC will use Amazon Cognito Identity to create a User Pool, you pay based on your monthly active users (MAUs) only. A user is counted as a MAU if, within a calendar month, there is an identity operation related to that user, such as sign-up, sign-in, token refresh, or password change. You are not charged for subsequent sessions or for inactive users within that calendar month. You will not be charged for first 50,000 users. For next 50,000 users you will be charged $0.0055, and after that for next 900,000 users $0,0046 a month per user. For more than 1 million users you will be charged @0.00325 and over 10 million users $0.0025 a month per user.



Creating AWS EC2 (WooComm-Vlado), installing Bitnami (LEMP), 
                  creating Domain name in NAmecheap.com and installingSSL/TLS Certificate(HTTPS)) 

Google Console:
1.Create Project to associate one App (user type -external (internal/external organization)), 
2.Create Credentials (OAuth Client ID(Web App), Client secret, Authorized JavaScript origins (Cognito URL), Authorized redirect URL (Cognito URL + oauth2/idpresponse).                                                       
3.Domain verification (domain, where our app’s running)
   
Amazon Cognito:
Create user pool: create app clients (who accesses pool)
                App integration (App client setting (enable identity provider (call back URL,
                                 sign out URL) OAuth2 flows and scope
               Amazon Cognito domain (check availability)
               Federation (Identity providers google, FB, Apple, Login with Amazon.. 
                            attribute mapping email)

