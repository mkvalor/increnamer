# incrinamer
A sample Python web service that produces host names with
embedded numbers based on supplied JSON params.

This service will return a single host name, per request, that
includes an encoded number.  The request will contain two param-
eters:

* A host IPV4 ip address
* A category for the host within the network
