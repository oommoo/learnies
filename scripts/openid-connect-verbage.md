From reading on OpenID Connect from okta, an identity provider for the internet

We have some clearly stated descriptions of serveral key concepts :

* Scopes
* Claims
* ID Token
* User info endpoint
* JWT (JSON Web Token)

# Scopes

Of the changes OpenID Connect brings and arguably one of the most important is a standard set of scopes. In the OAuth 2.0 specification, scopes are whatever the OAuth provider wants them to be. While this is flexible, it makes interoperability effectively impossible. OIDC standardizes these scopes to openid, profile, email, and address.

# Claims

In addition to standardizing the scopes used, OpenID Connect also standardizes the sets of claims for the OpenID Connect scopes. It is these standard sets of claims that contain the user specific information for authentication. For example, by having claims specifically named given_name and family_name, other systems from other organizations can create and receive user information in repeatable, predictable patterns.

# ID Token

For OpenID Connect, scopes can be used to request specific sets of information. This information is made available as claim values. The identity information in the ID token is specifically intended to be read by 3rd party applications to authenticate the same identity across multiple web applications, a crucial component of federation.

# User info endpoint

In addition to the ID token, with the implementation of OpenID Connect comes standardized endpoints. In particular, the /userinfo endpoint allows for the verification of identity information metadata and is key to interoperability with other OpenID Connect systems suitable for enterprise grade solutions.

# JWT (JSON Web Token)

JWT (pronounced j-o-t) is a cryptographically signed JSON payload that stores the user information. Using JWT’s allows information to be verified and trusted with a digital signature. With this trusted digital signature in place the information can later be verified using a signing key. OpenID Connect utilizes the JWT standard for the ID token.

