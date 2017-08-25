# Information

This repository holds maven repo for project https://github.com/wmlynar/rosjava_core/ which contain fix for xmlrpc multicall issue

This is how the repository was created

Forked rosjava and rosjava_mvn_repo projects

```
cd ~
mkdir -p rosjava_core_ws/src
cd rosjava_core_ws/src
git clone https://github.com/wmlynar/rosjava_core/
cd ..
catkin_make
source devel/setup.bash
cd devel/share/maven/
git clone https://github.com/wmlynar/rosjava_mvn_repo .
cd ../../..
cd src/rosjava_core/
pico package.xml  # update version <version>0.3.5-wmlynar</version>
./gradlew
./gradlew install
```

For local testing one can use following code in the pom.xml file

```
		<repository>
			<id>local-maven-repo</id>
			<url>file:///home/[username]/rosjava_core_ws/devel/share/maven</url>
		</repository>
```

# The RosJava Maven Repo

Maven artifact repository for rosjava dependencies and builds.

## Contents


**From Dependent Repositories**

Many of the artifacts here are collected from a variety of other repositories to provide a single stable source of artifacts for development of the rosjava/android core stacks. This list (hopefully relatively complete) includes:

* http://repo1.maven.org/maven2/org/apache/apache/
* http://repo1.maven.org/maven2/junit/junit/
* http://repo.maven.apache.org/maven2/org/sonatype/oss/oss-parent/
* http://repo.jfrog.org/artifactory/libs-releases/org/apache/commons/com.springsource.org.apache.commons.codec/
* http://repo.jfrog.org/artifactory/libs-releases/org/apache/commons/com.springsource.org.apache.commons.httpclient/
* http://repo.jfrog.org/artifactory/libs-releases/org/apache/commons/com.springsource.org.apache.commons.io/
* http://repo.jfrog.org/artifactory/libs-releases/org/apache/commons/com.springsource.org.apache.commons.lang/
* http://repo.jfrog.org/artifactory/libs-releases/org/apache/commons/com.springsource.org.apache.commons.logging/
* http://repo.jfrog.org/artifactory/libs-releases/org/apache/commons/com.springsource.org.apache.commons.net/
* http://central.maven.org/maven2/org/apache/commons/commons-parent/
* http://central.maven.org/maven2/ws-commons-util/ws-commons-util/
* http://central.maven.org/maven2/com/google/guava/guava/
* http://central.maven.org/maven2/com/google/guava/guava-parent/
* http://central.maven.org/maven2/com/google/code/findbugs/jsr305/
* http://central.maven.org/maven2/io/netty/netty/
* http://central.maven.org/maven2/io/netty/netty-all/
* http://central.maven.org/maven2/xml-apis/xml-apis/
* http://central.maven.org/maven2/commons-pool/commons-pool/
* http://central.maven.org/maven2/org/apache/commons/commons-pool2/
* http://central.maven.org/maven2/dnsjava/dnsjava/
* http://jcenter.bintray.com/com/android/tools/build/gradle/

**Official RosJava Artifacts**

All official rosjava artifacts that are generated have their official maven home here.

**Interesting 3rd Party Dependencies**

We also include some esoteric, but useful 3rd party dependencies here that the community may find useful. Some of these are custom built and added here. Others come from the following list of repositories:

## Other Maven Repositories

Some other maven repositories that may be of interest to ros users:

* http://central.maven.org/maven2/org/bytedeco/javacpp-presets/opencv/
* http://central.maven.org/maven2/nu/pattern/opencv/

