# firebase-auth

Use of Firebase Auth facilities

## Authentication and Authorization

- Authentication is the process of verifying who a user is.
- Authorization is the process of verifying what a user can access.

### Authentication using Firebase

  - Firebase has its own ***email* and *password*** authentication system.
  - Firebase also has a ***federated identity provider integration***, allowing users to sign in with their ***Google***, ***Facebook***, ***Twitter***, and ***GitHub*** accounts.
    - There are also available other providers, like ***Yahoo*** (*OAuth*), ***iPhone*** (*OAuth 2.0*) or ***Microsoft*** (both *Azure Active Directory* and *personal Microsoft accounts*).
  - Moreover, *custom* and *phone number* authentications are also possible, as well as *anonymous accounts* which can be transformed into *authenticated user accounts*.
  - This software now only uses firebase own authentication system, but may be it could be expanded in the future for other authentication systems. *Google*, *Yahoo* and also *iPhone* are the most rellevant ones, but *anonymous accounts* are a very powerful feature to take into account.

## Security Rules

 Security Rules are used by ***Cloud Firestore***, *Cloud Storage for Firebase*, and the *Realtime Database* to perform **authorization**; they determine if a user can perform a given ***read*** or ***write***.

### The admin Web API

The *admin SDK* bypasses *Firebase Security Rules* and should only be used from a trusted environment like Firebase Functions or a server you control.

It depends on a ***secret key*** for the *web app's Firebase configuration*, and it must remain secret. So its only useful to be used **server side**, but **never on public code web servers**.

It is **very important**, as the ***admin SDK* bypasses *Firebase Security Rules***.

## App Check

