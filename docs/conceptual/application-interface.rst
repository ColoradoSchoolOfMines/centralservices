Application Interface
=====================

Central Services provides an API for application developers to utilize data
stored in Central Services. This API is called the **Central Services
Application API**.

Some examples of applications which might want to access data in Central
Services are:

- **Club Websites:** a club might want to use Central Services to get
  information about the users of the club website.

The Application API has three tiers:

1. **Public:** provides access to all public information. This should be
   sufficient for most applications.
2. **Privileged:** provides the ability to access private information with
   express, granular permission of the user. This should be sufficient for
   applications which may need private user data.
3. **Trusted:** provides access to all public and private information without
   needing express per-user permission grants. This should be used to create
   portals to Central Services such as the Central Services User Portal.

Both the Privileged and Trusted tier require the application developer to
request an Application API key.

Requesting an Application API Key
---------------------------------

To create an application that uses the Privileged or Trusted tiers, the
application developer must request an Application API key. Application API key
requests are approved or disapproved by the administrator of Central Services
(see `Security Model`_ for more details on how this process will work). The
application developer can request their Application API key to be either
Privileged or Trusted.

Application API keys can be revoked at any time, and for any reason, by the
Central Services administrator. Application API keys can also be converted from
Privileged to Trusted, and vice versa.

Accessing the Application API
-----------------------------

The Central Services Application API is a REST API. It is accessible via the
Central Services Application API HTTPS endpoint. The Application API is
documented `here`_.

Privileged and Trusted tier Application API calls have a required `api_key`
query parameter.  The Public tier endpoints can be accessed without such a key
(if a key is provided, it will be ignored).

.. _here: ../applicaton-api-specification.html

Requesting User Data as a Privileged Tier Application
-----------------------------------------------------

When an application wants to request information about a user, they will
redirect the user to the Central Services Application Authorization page passing
some metadata about what information the application wants to access.

Security Model
--------------

Central Services will manage whether or not an given Application API key is
Privileged or Trusted. Central Services will also keep track of which Privileged
applications have access to which users' data.

Users will be able to control the data that each application can access. Note,
however, that once a user grants access to personal information to a certain
application, then the application can store it internally.

.. TODO: What is an Application

.. TODO: What is an API Key
