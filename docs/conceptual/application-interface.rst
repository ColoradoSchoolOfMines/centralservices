Application Interface
=====================

Applications may wish to utilize data stored in Central Services. Such
applications can do so using the Central Services API.

The API has three tiers:

1. **Public:** provides access to all public information. This should be
   sufficient for most applications.
2. **Privileged:** provides the ability to access access to private information
   with express, granular permission of the user. This should be sufficient for
   applications which may need private user data.
3. **Trusted:** provides access to all public and private information without
   needing express per-user permission grants. This should be used to create
   Central Services portals such as the Central Services User Portal.

Both the Privileged and Trusted tier require the application developer to
request an application API key.

Requesting an API Key
---------------------

To create an application that uses the Privileged or Trusted tiers, the
application developer must request an application API key. API key requests are
approved or disapproved by the administrator of Central Services (see `Security
Model`_ for more details on how this process will work). The application
developer can request their API key to be either Privileged or Trusted.

Application API keys can be revoked at any time, for any reason, by the Central
Services administrator. Application API keys can also be changed from Privileged
to Trusted, and vice versa.

Accessing the API
-----------------

The Central Services API is a REST API. It is accessible via the central
services API endpoint at `https://central.mines.edu/api`. The API is documented
`here`_.

Privileged and Trusted tier endpoints have a required `api_key` query parameter.
The Public tier endpoints can be accessed without such a key.

.. _here: ../api-specification.html

Security Model
--------------

Central Services will manage whether or not an given application API key is
Privileged or Trusted.

.. TODO: What is an Application

.. TODO: What is an API Key
