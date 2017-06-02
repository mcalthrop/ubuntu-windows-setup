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
sudo apt-get install git
# check installation:
git --version
```

### Java 8 JDK

```bash
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
# check installation:
java -version
javac -version
```

> source: [http://www.webupd8.org/2012/09/install-oracle-java-8-in-ubuntu-via-ppa.html](http://www.webupd8.org/2012/09/install-oracle-java-8-in-ubuntu-via-ppa.html)

### Maven

```bash
sudo apt-get install maven
# check installation:
mvn --version
```

## Removing packages

Most packages are removed in the standard way:

```bash
sudo apt-get remove <package-name>
```

However, Java 8 was a bit different:

```bash
sudo apt-get remove oracle-java8-installer
sudo apt-get purge oracle-java8-installer
sudo apt-get autoremove
```

> source: [https://askubuntu.com/a/850740](https://askubuntu.com/a/850740)
