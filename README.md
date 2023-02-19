# firebase-auth

Use of Firebase Auth facilities

## Authentication and Authorization

- **Authentication** is the process of verifying who a user is.
- **Authorization** is the process of verifying what a user can access.

### Authentication using Firebase

  - Firebase has its own ***email* and *password*** authentication system.
  - Firebase also has a ***federated identity provider integration***, allowing users to sign in with their ***Google***, ***Facebook***, ***Twitter***, and ***GitHub*** accounts.
    - There are also available other providers, like ***Yahoo*** (*OAuth*), ***iPhone*** (*OAuth 2.0*) or ***Microsoft*** (both *Azure Active Directory* and *personal Microsoft accounts*).
  - Moreover, ***custom*** and ***phone number*** authentications are also possible, as well as ***anonymous accounts*** which can be transformed into *authenticated user accounts*.
    - The *anonymous accounts* are a very powerful feature.
  - This software now only uses *firebase own authentication system*, but in the future it could be expanded for other authentication systems.

## Security Rules

 Security Rules are used by ***Cloud Firestore***, ***Cloud Storage for Firebase***, and the ***Realtime Database*** to **perform authorization**; they determine if a user can perform a given ***read*** or ***write***.

### The admin Web API

The *admin SDK* bypasses *Firebase Security Rules* and should only be used from a trusted environment like Firebase Functions or a server you control.

It depends on a ***secret key*** for the *web app's Firebase configuration*, and it must remain secret. So its only useful to be used **server side**, but **never on public code web servers**.

It is **very important**, as the ***admin SDK* bypasses *Firebase Security Rules***; so, it must be used very carefully.

## App Check

*App Check* verifies that a request originated from your app and blocks all other requests to backend resources. It can be used to protect ***Firebase APIs*** and ***API endpoints on your own server***.

On Web applications it is implemented using ***Google reCAPTCHA*** which is automatically managed by the *Firebase API*.

## Implementations

1. [firebase-auth-serverless-version](https://github.com/S-Cesc/firebase-auth-client-version): Browser only (javascript) implementation. The *Bootstrap Studio* file for the serverless version is found on this repository; its own repository has the exported version, available without the *Bootstrap Studio*.
2. [firebase-auth-server-version](https://github.com/S-Cesc/firebase-auth-server-version): Express node (javascript) server implementation.
