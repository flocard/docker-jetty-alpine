# Purpose 

Trying to use jetty official Image  (https://hub.docker.com/_/jetty) to run legacy Jetty/JRE8 application in a Openshift container, but facing to some issues :

- https://github.com/docker-library/openjdk/pull/322 : 

no more OpenJDK 8 Alpine images (Alpine/musl is not officially supported by the OpenJDK project, so this reflects that -- see "Project Portola" for the Alpine porting efforts which I understand are still in need of help).

Without update, there is no official image passing vulnerabilities scan (trivy)

- Official image doesn't support "Arbitrary User IDs" security constraint required by openshift (https://docs.openshift.com/container-platform/3.11/creating_images/guidelines.html)

