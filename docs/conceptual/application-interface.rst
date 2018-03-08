Application Interface
=====================

Applications may wish to utilize data stored in Central Services. Such
applications can do so using the Central Services API.

The API has three tiers:

1. **Public API:** This API provides access to all public information.
2. **Privileged API:** This API provides the ability to access access to private
   information with express, granular permission of the user.
3. **Trusted API:** This API provides access to all public and private
   information without needing express per-user permission grants.

Both the Privileged and Trusted APIs require the application developer to
request an application API key.

Requesting an API Key
---------------------

To create an application that uses the Privileged or Trusted APIs, the
application developer must request an application API key. API key requests are
approved or disapproved by the administrator of Central Services (see `Security
Model`_ for more details on how this process will work). The application
developer can request their API key to be either Privileged or Trusted.

Accessing the API
-----------------

The Central Services API is a REST API. It is accessible via the central
services API endpoint at `https://central.mines.edu/api`. The API is documented
`here`_.

.. _here: ../api-specification.html

Security Model
--------------

Central Services will manage whether or not an given application API key is
Privileged or Trusted.

.. TODO: What is an Application

.. TODO: What is an API Key
