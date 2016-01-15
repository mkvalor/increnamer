# incrinamer
A sample Python web service that produces host names with
embedded numbers based on supplied JSON params.

This service will return a single host name (per request) that
includes an encoded number.  The request will contain two param-
eters:

* A host IP address (in IPV4 format)
* A role category for the host within the network

The service will gracefully handle re-submission of the same
ip address by taking appropriate actions based on the role
parameter:

* If the re-cycled IP address is submitted with the same
role as before, then the pre-existing hostname associated
with that IP address will be returned.

* If the recycled IP address is submitted with the a new role
category, its old hostname will be recycled and will become
available for re-use by a subsequent request for that role.
A new hostname will be constructed with the lowest available
embedded number available for that role.
