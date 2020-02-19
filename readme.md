# Okta as an Identity provider for B2C

This repository contains examples of how to integrate Okta as an external idenity provider with Azure B2C using custom policies

## Quickstart:

Follow the external identity provider steps for a Microsoft Account found here:
https://docs.microsoft.com/en-us/azure/active-directory-b2c/identity-provider-microsoft-account-custom?tabs=applications

Instead of adding an application in Azure AD, add the application in Okta and set the following

Login redirect URI: https://{yourb2ctenantname}.b2clogin.com/{yourb2ctenantname}.onmicrosoft.com/oauth2/authresp


### Change the following settings in the B2C Claims provider

Okta OpenId Connect Settings in B2C Policy:

ProviderName: https://{yourOktaTenant}/oauth2/default

METADATA: https://{yourOktaTenant}/oauth2/default/.well-known/openid-configuration


<hr/>

## Full guide:

Coming soon