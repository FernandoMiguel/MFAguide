# MFA guide

## Introduction
Multi-Factor or Two-step verification is a method of authentication that requires more than one verification method and adds a critical second layer of security to user sign-ins. It works by requiring any two or more of the following verification methods:
* Something you know (typically a password)
* Something you have (a trusted device that is not easily duplicated, like a phone)
* Something you are (biometrics)
![alt text](https://docs.microsoft.com/en-us/azure/multi-factor-authentication/media/multi-factor-authentication/phone.png "mfa")


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

### 2FA apps

### Physical tokens

### Recovery

Both physical and virtual tokens are possible of being lost or malfunction. 

To prevent loss of access to the user account when the MFA token is not available, **printed codes** are availble on most services.

The user should print them, and keep them safe.


## Guides

* Google Accounts https://authy.com/guides/gmail/


# Sources

https://docs.microsoft.com/en-us/azure/multi-factor-authentication/multi-factor-authentication

http://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa.html

