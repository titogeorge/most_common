keytool
-------------
See all the certificates in key store. 
```sh
$ keytool -list -v -keystore /usr/lib/jvm/java-8-openjdk-amd64/jre/lib/security/cacerts
```
> **Note:**

> - Change the file path
> - What is [keytool?](http://docs.oracle.com/javase/7/docs/technotes/tools/solaris/keytool.html)

Maven
-------------
Set mvn pom version to latest git commit.
```sh
mvn versions:set -DgenerateBackupPoms=false -DnewVersion=myproject-`git rev-parse --abbrev-ref HEAD`-`git log -n 1 --pretty=format:'%H'`
```

> **Note:**

> - Used with CD tool to easily root-cause "My code not deployed" Bug 
> - Sets version in format '**myproject-branch_name-commit_hash**'

[Markdown by StackEdit](https://stackedit.io/)
