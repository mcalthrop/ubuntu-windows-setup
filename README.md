# ubuntu-windows-setup

_I recently had to set up Ubuntu on Windows 10; here are some things I found useful._

## Installation

Do the following:

- make sure you are running Windows 10
- get the [Windows 10 anniversary update](https://blogs.windows.com/windowsexperience/2016/08/02/how-to-get-the-windows-10-anniversary-update/)
- [install the Linux bash shell](https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/)

## Setup

Here are the packages that I installed.

### Git

```bash
$ sudo apt-get install git
# check installation:
$ git --version
git version 1.9.1
```

### Java 8 JDK

```bash
$ sudo add-apt-repository ppa:webupd8team/java
$ sudo apt-get update
$ sudo apt-get install oracle-java8-installer
# check installation:
$ java -version
java version "1.8.0_131"
Java(TM) SE Runtime Environment (build 1.8.0_131-b11)
Java HotSpot(TM) 64-Bit Server VM (build 25.131-b11, mixed mode)
$ javac -version
javac 1.8.0_131
```

> source: [http://www.webupd8.org/2012/09/install-oracle-java-8-in-ubuntu-via-ppa.html](http://www.webupd8.org/2012/09/install-oracle-java-8-in-ubuntu-via-ppa.html)

### Maven

```bash
$ sudo apt-get install maven
# check installation:
$ mvn --version
Apache Maven 3.0.5
Maven home: /usr/share/maven
Java version: 1.8.0_131, vendor: Oracle Corporation
Java home: /usr/lib/jvm/java-8-oracle/jre
Default locale: en_GB, platform encoding: UTF-8
OS name: "linux", version: "3.4.0+", arch: "amd64", family: "unix"
```

## Removing packages

Most packages are removed in the standard way:

```bash
$ sudo apt-get remove <package-name>
```

However, Java 8 was a bit different:

```bash
$ sudo apt-get remove oracle-java8-installer
$ sudo apt-get purge oracle-java8-installer
$ sudo apt-get autoremove
```

> source: [https://askubuntu.com/a/850740](https://askubuntu.com/a/850740)
