---
layout: default_md
title: ActiveMQ Classic 5.7.0 Release
title-class: page-title-classic
type: classic
redirect_from:
- /../../../activemq-570-release
- /../../../activemq-5007000-release
---

<div class="alert alert-warning">
  This is an older release. To get the current release, please see the <a href="{{site.baseurl}}/components/classic/download" class="alert-link">download page</a>.
</div>

Apache ActiveMQ Classic 5.7.0 is primarily a maintenance release which resolves nearly [200 issues](https://issues.apache.org/jira/secure/IssueNavigator.jspa?reset=true&jqlQuery=project+%3D+AMQ+AND+fixVersion+%3D+%225.7.0%22+AND+status+%3D+Resolved+ORDER+BY+priority+DESC&mode=hide), mostly bug fixes and improvements

*   Java 7 support (compiled with jdk6 and validated with jdk7)
*   [Secure WebSockets (wss) transport](http://activemq.apache.orgConnectivityConnectivity/Connectivity/websockets.md#WebSockets-SecureWebSockets)
*   [Broker Based Redelivery](http://activemq.apache.orgDevelopers/Developer Guide/Design Documents/message-redelivery-and-dlq-handling.md#MessageRedeliveryandDLQHandling-BrokerRedelivery%28v5.7%29)
*   [Pluggable Store Lockers](http://activemq.apache.orgFeatures/PersistenceFeatures/Persistence/Features/Persistence/pluggable-storage-lockers)
*   [Lease based database locker](http://activemq.apache.orgFeatures/PersistenceFeatures/Persistence/Features/Persistence/pluggable-storage-lockers.md#Pluggablestoragelockers-LeaseDatabaseLocker)
*   Set a [RedeliveryPolicy per destination](http://activemq.apache.orgFeatures/Consumer Features/redelivery-policy.md#RedeliveryPolicy-RedeliveryPolicyperDestination)
*   Includes [Apache Camel 2.10](http://camel.apache.org/camel-2100-release.html)

Getting the Binary Distributions
--------------------------------

Description|Download Link|PGP Signature file of download
Windows Distribution|[apache-activemq-5.7.0-bin.zip](http://archive.apache.org/dist/activemq/apache-activemq/5.7.0/apache-activemq-5.7.0-bin.zip)|[apache-activemq-5.7.0-bin.zip.asc](http://archive.apache.org/dist/activemq/apache-activemq/5.7.0/apache-activemq-5.7.0-bin.zip.asc)
Unix/Linux/Cygwin Distribution|[apache-activemq-5.7.0-bin.tar.gz](http://archive.apache.org/dist/activemq/apache-activemq/5.7.0/apache-activemq-5.7.0-bin.tar.gz)|[apache-activemq-5.7.0-bin.tar.gz.asc](http://archive.apache.org/dist/activemq/apache-activemq/5.7.0/apache-activemq-5.7.0-bin.tar.gz.asc)

Verify the Integrity of Downloads
---------------------------------

It is essential that you verify the integrity of the downloaded files using the PGP or MD5 signatures. The PGP signatures can be verified using PGP or GPG. Begin by following these steps:

1.  Download the [KEYS](http://www.apache.org/dist/activemq/KEYS)
2.  Download the asc signature file for the relevant distribution
3.  Verify the signatures using the following commands, depending on your use of PGP or GPG:
    ```
    $ pgpk -a KEYS
    $ pgpv apache-activemq-<version>-bin.tar.gz.asc
    ```
    or
    ```
    $ pgp -ka KEYS
    $ pgp apache-activemq-<version>-bin.tar.gz.asc
    ```
    or
    ```
    $ gpg --import KEYS
    $ gpg --verify apache-activemq-<version>-bin.tar.gz.asc
    ```

(Where <version> is replaced with the actual version, e.g., 5.1.0, 5.2.0, etc.).

Alternatively, you can verify the MD5 signature on the files. A Unix program called `md5` or `md5sum` is included in most Linux and Unix distributions. It is also available as part of [GNU Textutils](http://www.gnu.org/software/textutils/textutils.html). Windows users can utilize any of the following md5 programs:

*   [md5](http://www.fourmilab.ch/md5/)
*   [md5sums](http://www.pc-tools.net/win32/md5sums/)
*   [SlavaSoft FSUM](http://www.slavasoft.com/fsum/)

Getting the Binaries using Maven 2
----------------------------------

To use this release in your maven project, the proper dependency configuration that you should use in your [Maven POM](http://maven.apache.org/guides/introduction/introduction-to-the-pom.html) is:
```
<dependency>
  <groupId>org.apache.activemq</groupId>
  <artifactId>activemq-core</artifactId>
  <version>5.7.0</version>
</dependency>
```

Getting the Source Code
-----------------------

### Source Distributions

Description|Download Link|PGP Signature file of download
---|---|---
Source Release|[activemq-parent-5.7.0-source-release.zip](http://archive.apache.org/dist/activemq/apache-activemq/5.7.0/activemq-parent-5.7.0-source-release.zip)|[activemq-parent-5.7.0-source-release.zip.asc](http://archive.apache.org/dist/activemq/apache-activemq/5.7.0/activemq-parent-5.7.0-source-release.zip.asc)

### SVN Tag Checkout

```
svn co http://svn.apache.org/repos/asf/activemq/tags/activemq-5.7.0
```

Changelog
---------

For a more detailed view of new features and bug fixes, see the [release notes](https://issues.apache.org/jira/secure/ReleaseNote.jspa?projectId=12311210&version=12321258)

Also see the previous [ActiveMQ Classic 5.6.0 Release](classic-05-06-00)

