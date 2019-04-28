# JMeter base docker image

In distributed testing, all the environment are expected to have same version of Java, JMeter, plugins etc. Only difference between the master and slave would be the ports which are exposed and process running. So, Lets create a Dockerfile which has all the common steps for both master and slave. Lets call it as jmeter base image and we would need to do the followings to build our base image.

* We need Java8 – so lets openjdk-8-jre version to keep size as less as possible
* We might need few utilities like tzdata curl unzip bash etc. So lets install them.
* We need latest version of JMeter. Create a variable for version – so that maintenance would be easier in future.