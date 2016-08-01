# LoadBalancerTomcat
https://www.youtube.com/watch?v=9gtpyqhd-NI

https://www.mulesoft.com/tcat/tomcat-clustering

A clustered architecture is used to solve one or more of the following problems:

A single server cannot handle the high number of incoming requests efficiently
A stateful application needs a way of preserving session data if its server fails
A developer requires the capability to make configuration changes or deploy updates to their applications without discontinuing service.
A clustered architecture solves these problems using a combination of load balancing, multiple server "workers" to process the balanced load, and some kind of session replication. Depending on the needs of the application, only some of these components may be used, or additional components such as caching and compression engines.

Since this is a how-to guide, we'll stop the general information session here, and move on to setting up a working Tomcat cluster. However, if you're new to clustering, it's probably a good idea to do a little more reading up on the subject.

For more information about the how and why of clustered architecture, check out our Tomcat Clustering Basics article for an in-depth look at all the components of a cluster, comparisons of different approaches, and more.


or the purposes of this tutorial, we'll use a simple clustered configuration:

Apache HTTPD with mod_jk (for load balancing)
2 Tomcat 6.x instances
in-memory session replication (via Tomcat's built in functionality)
