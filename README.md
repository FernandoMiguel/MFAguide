# MFA guide

## Introduction

Multi-Factor or Two-step verification is a method of authentication that requires more than one verification method and adds a critical second layer of security to user sign-ins. It works by requiring any two or more of the following verification methods:
* Something you know (typically a password)
* Something you have (a trusted device that is not easily duplicated, like a phone)
* Something you are (biometrics)


### Methods available for two-step verification

When a user signs in, an additional verification is sent to the user. The following are a list of methods that can be used for this second verification.

* Phone call

   A call is placed to a user’s registered phone. The user enters a PIN if necessary then presses the # key.

* Text message

   A text message is sent to a user’s mobile phone with a six-digit code. The user enters this code on the sign-in page.

* Mobile app notification

   A verification request is sent to a user’s smart phone. The user enters a PIN if necessary then selects Verify on the mobile app.

* Mobile app verification code

   The mobile app, which is running on a user’s smart phone, displays a verification code that changes every 30 seconds. The user finds the most recent code and enters it on the sign-in page.

* Third-party OATH tokens

   Physical tokens like Yubikey

## Physical vs Virtual tokens

MFA tokens can be split into three categories.

* Call/SMS
* Virtual tokens
* Physical tokens

#### SMS
Within the security community and governance bodies, the use of SMS/Text or Phone calls as Out of band verification is no longer recommended as two-factor authentication, because of their many insecurities.

https://www.schneier.com/blog/archives/2016/08/nist_is_no_long.html

#### Virtual tokens

Virtual tokens are the easiest to use, as usually the user has an app on their smartphone and will be able to either copy the token in the device itself to another app, or type on another device/computer.

#### Physical tokens

Physical tokens are one of the more secure form, given they can't typically be copied/cloned.

They can be available in the form of credit card format or keychains with LCD displays, or USB-(A/C) dongles.

Recently NFC based dongles appeared in the market, but their support is very limited. 

https://www.theverge.com/2017/1/26/14397276/facebook-two-factor-nfc-security-key-account-hack

### 2FA apps

The most common MFA apps are:

* Authy https://authy.com/download/
* Google Authenticator https://support.google.com/accounts/answer/1066447
* Microsoft Authenticator https://docs.microsoft.com/azure/multi-factor-authentication/end-user/microsoft-authenticator-app-how-to
* LastPass Authenticator https://lastpass.com/multifactor-authentication/
* DUO https://duo.com/product/trusted-users/two-factor-authentication/duo-mobile

### Physical tokens

The most common MFA apps are:

* Yubiko Yubikeys https://www.yubico.com/store/
* Gemalto Safenet https://safenet.gemalto.com/multi-factor-authentication/authenticators/
* RSA SecurID  http://www.tokenguard.com/RSA-SecurID-Hardware.asp

### Recovery

Both physical and virtual tokens are possible of being lost or malfunction. 

To prevent loss of access to the user account when the MFA token is not available, **printed codes** are availble on most services.

The user should print them, and keep them safe.

## Guides

* Google Accounts https://authy.com/guides/gmail/
* Github https://authy.com/guides/github/
* Slack  https://authy.com/guides/slack/
* Facebook  https://authy.com/guides/facebook/
* Twitter   https://authy.com/guides/twitter/
* Dropbox https://authy.com/guides/dropbox/
* Amazon https://authy.com/guides/amazon/

# Sources

https://docs.microsoft.com/en-us/azure/multi-factor-authentication/multi-factor-authentication

http://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa.html

https://www.facebook.com/notes/facebook-security/security-key-for-safer-logins-with-a-touch/10154125089265766/
