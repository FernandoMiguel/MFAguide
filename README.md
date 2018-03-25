# MFA guide

**TL:DR  [Jump to the Guides](#guides)**

or keep on reading 

<!-- TOC -->

- [MFA guide](#mfa-guide)
    - [Introduction](#introduction)
        - [Methods available for two-step verification](#methods-available-for-two-step-verification)
        - [Site or Service support](#site-or-service-support)
        - [Protocols](#protocols)
    - [Physical vs Virtual tokens](#physical-vs-virtual-tokens)
            - [SMS](#sms)
            - [Virtual tokens](#virtual-tokens)
            - [Physical tokens](#physical-tokens)
    - [MFA apps](#mfa-apps)
    - [Physical tokens](#physical-tokens-1)
    - [Recovery](#recovery)
- [Guides](#guides)
- [Sources](#sources)

<!-- /TOC -->

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

   A verification request is sent to a user’s smartphone. The user enters a PIN if necessary then selects Verify on the mobile app.

* Mobile app verification code

   The mobile app, which is running on a user’s smartphone, displays a verification code that changes every 30 seconds. The user finds the most recent code and enters it on the sign-in page.

* Third-party OATH tokens

   Physical tokens like Yubikey

### Site or Service support

Sadly not every online service provides the user with the means to secure their sign-in.

The following site lists the state of many sites as to if they support or not MFA:

**[https://twofactorauth.org/](https://twofactorauth.org/)**

### Protocols

* TOTP
The Time-based One-Time Password algorithm (TOTP) is an algorithm that computes a one-time password from a shared secret key and the current time.

[From the Wikipedia:](https://en.wikipedia.org/wiki/Time-based_One-time_Password_Algorithm)

> TOTP is an example of a hash-based message authentication code (HMAC). It combines a secret key with the current timestamp using a cryptographic hash function to generate a one-time password. Because network latency and out-of-sync clocks can result in the password recipient having to try a range of possible times to authenticate against, the timestamp typically increases in 30-second intervals, which thus cuts the potential search space.

> In a typical two-factor authentication application, user authentication proceeds as follows: a user enters username and password into a website or other server, generates a one-time password for the server using TOTP running locally on a smartphone or other device, and types that password into the server as well. The server then also runs TOTP to verify the entered one-time password. For this to work, the clocks of the user's device and the server need to be roughly synchronized (the server will typically accept one-time passwords generated from timestamps that differ by ±1 time interval from the client's timestamp). A single secret key, to be used for all subsequent authentication sessions, must have been shared between the server and the user's device over a secure channel ahead of time. If some more steps are carried out, the user can also authenticate the server using TOTP.

* HOTP
HOTP is an HMAC-based one-time password (OTP) algorithm. 

The main difference between HOTP and TOTP is that the HOTP passwords can be valid for an unknown amount of time, while the TOTP passwords keep on changing and are only valid for a short window in time. Because of this difference generally speaking the TOTP is considered as a more secure One-Time Password solution.

* U2F
U2F is an open authentication standard that enables internet users to securely access any number of online services, with one single device, instantly and with no drivers, or client software needed.

U2F was created by Google and Yubico. The technical specifications are hosted by the open-authentication industry consortium known as the [FIDO Alliance](https://fidoalliance.org/) .

A list of services that use FIDO U2F:

[https://www.yubico.com/solutions/#FIDO-U2F](https://www.yubico.com/solutions/#FIDO-U2F)

## Physical vs Virtual tokens

MFA tokens can be split into three categories.

* Call/SMS
* Virtual tokens
* Physical tokens

#### SMS
Within the security community and governance bodies, the use of SMS/Text or Phone calls as Out of band verification is no longer recommended as two-factor authentication, because of their many insecurities.

[https://www.schneier.com/blog/archives/2016/08/nist_is_no_long.html
](https://www.schneier.com/blog/archives/2016/08/nist_is_no_long.html
)

#### Virtual tokens

Virtual tokens are the easiest to use, as usually the user has an app on their smartphone and will be able to either copy the token in the device itself to another app, or type on another device/computer.

#### Physical tokens

Physical tokens are one of the more secure form, given they can't typically be copied/cloned.

They can be available in the form of credit card format or keychains with LCD displays, or USB-(A/C) dongles.

Recently, NFC based dongles appeared in the market, but their support is very limited. 

[https://www.theverge.com/2017/1/26/14397276/facebook-two-factor-nfc-security-key-account-hack](https://www.theverge.com/2017/1/26/14397276/facebook-two-factor-nfc-security-key-account-hack)

## MFA apps

The most common MFA apps are:

* Authy [https://authy.com/download/](https://authy.com/download/)
* Google Authenticator [https://support.google.com/accounts/answer/1066447](https://support.google.com/accounts/answer/1066447)
* Microsoft Authenticator [https://docs.microsoft.com/azure/multi-factor-authentication/end-user/microsoft-authenticator-app-how-to](https://docs.microsoft.com/azure/multi-factor-authentication/end-user/microsoft-authenticator-app-how-to)
* LastPass Authenticator [https://lastpass.com/multifactor-authentication/](https://lastpass.com/multifactor-authentication/)
* DUO [https://duo.com/product/trusted-users/two-factor-authentication/duo-mobile](https://duo.com/product/trusted-users/two-factor-authentication/duo-mobile)

## Physical tokens

The most common physical MFA tokens are:

* Yubiko Yubikeys [https://www.yubico.com/store/](https://www.yubico.com/store/)
* Gemalto Safenet [https://safenet.gemalto.com/multi-factor-authentication/authenticators/](https://safenet.gemalto.com/multi-factor-authentication/authenticators/)
* RSA SecurID  [https://www.tokenguard.com/RSA-SecurID-Hardware.asp](https://www.tokenguard.com/RSA-SecurID-Hardware.asp)

## Recovery

Both physical and virtual tokens can be lost or malfunction. 

To prevent loss of access to the user account when the MFA token is not available, **printed codes** are available on most services.

The user should print them, and keep them safe.

# Guides

* Google Accounts [https://authy.com/guides/gmail/](https://authy.com/guides/gmail/)
* Slack  [https://authy.com/guides/slack/](https://authy.com/guides/slack/)
* Facebook  [https://authy.com/guides/facebook/](https://authy.com/guides/facebook/)
* Twitter   [https://authy.com/guides/twitter/](https://authy.com/guides/twitter/)
* Dropbox [https://authy.com/guides/dropbox/](https://authy.com/guides/dropbox/)
* Amazon [https://authy.com/guides/amazon/](https://authy.com/guides/amazon/)
* GitHub [https://authy.com/guides/github/](https://authy.com/guides/github/)
* GitHub [MFA and tricks](github.md)

# Sources

[https://docs.microsoft.com/en-us/azure/multi-factor-authentication/multi-factor-authentication](https://docs.microsoft.com/en-us/azure/multi-factor-authentication/multi-factor-authentication)

[https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa.html)

[https://www.facebook.com/notes/facebook-security/security-key-for-safer-logins-with-a-touch/10154125089265766/](https://www.facebook.com/notes/facebook-security/security-key-for-safer-logins-with-a-touch/10154125089265766/)

[https://aws.amazon.com/iam/details/mfa/](https://aws.amazon.com/iam/details/mfa/)

[https://help.github.com/articles/about-two-factor-authentication/](https://help.github.com/articles/about-two-factor-authentication/)

[https://www.yubico.com/solutions/fido-u2f/](https://www.yubico.com/solutions/fido-u2f/)
