# Okta as an Identity provider for B2C

This repository contains examples of how to integrate Okta as an external idenity provider with Azure B2C using custom policies
<hr/>

## Policy Overviews:

**SignUpSignInOkta Policy**

Allows the user to sign in using any of the following:
* Local Account
* Okta
* Microsoft Live Account

After first sign-in, the user may enter their name information

**SignUpSignInOktaDefault Policy**

Only allows sign in using Okta. If someone is already authenticated, B2C will not prompt again


**SignInLinkLocalToOkta Policy**

Allows a user to sign in or create a local account and then link that to an Okta account


**SignInLinkOktaToLocal Policy**

Allows a user to sign in with Okta and then create a new local account to link to or link to an existing local account
<hr/>

## Quickstart:

Follow the external identity provider steps for a Microsoft Account found [here](https://docs.microsoft.com/en-us/azure/active-directory-b2c/identity-provider-microsoft-account-custom?tabs=applications "b2c identity providers")


Instead of adding an application in Azure AD, add the application in Okta and set the following

__**Login redirect URI:**__ https://{yourb2ctenantname}.b2clogin.com/{yourb2ctenantname}.onmicrosoft.com/oauth2/authresp


### Change the following settings in the B2C Claims provider

Okta OpenId Connect Settings in B2C Policy:

__**ProviderName:**__ https://{yourOktaTenant}/oauth2/default

__**METADATA:**__ https://{yourOktaTenant}/oauth2/default/.well-known/openid-configuration


<hr/>

## Full guide:

Coming soon