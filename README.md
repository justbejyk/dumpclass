# Dumpclass
Dump classes from running JVM process by sa-jdi.jar.

Support wildcard match.


### Download dumpclass.jar

Can download dumpclass.jar from releases page.

https://github.com/hengyunabc/dumpclass/releases

```bash
wget https://github.com/hengyunabc/dumpclass/releases/download/0.0.1/dumpclass.jar
```

### Usage

```
Usage:
 java -jar dumpclass.jar <pid> <pattern> [outputDir]

pattern: support ? * wildcard match.
outputDir: default outputDir is current directory.

Example:
 java -jar dumpclass.jar 4345 *StringUtils
 java -jar dumpclass.jar 4345 *StringUtils /tmp

Use the specified sa-jdi.jar:
 java -cp "./dumpclass.jar:$JAVA_HOME/lib/sa-jdi.jar" io.github.hengyunabc.dumpclass.DumpMain <pid> <pattern> [outputDir]
```

### complie dumpclass.jar

```bash
mvn clean package
ls -alh target
```