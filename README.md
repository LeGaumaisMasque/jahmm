# JAHMM

> This repository is for the most part a simple clone of the former
> Google code repository. The documentation and examples still have
> to be imported.

Jahmm is a Java library implementing the various, well-known algorithms
related to Hidden Makov Models (HMMs for short).

This library is under the BSD license.

This library is short and simple.  It's been written for clarity.  It
is particularly well suited for research and academic use.



## Compiling

To compile the library, you simply need to compile all the files held
in the src/main/java directory.  Thus, simply calling 'javac' with all the
.java files held in the 'src' directory as arguments compiles everything.

Compiling can be done using the 'maven' build tool (see maven.apache.org) by
typing 'mvn compile' in the root directory of the distribution (where the
'pom.xml' file resides).

This can also be done using `ant` (see http://ant.apache.org/) by
typing `ant` in the root directory of the distribution (where the 'build.xml'
file resides).

Jahmm requires Java 1.5.0.

The generated .class files will be put in the 'target/classes' directory.



## Running

Notice that if you just want to try the library, you don't have to
compile it.  '.jar' files for each jahmm release are available on the
website; to use it, simply launch:
```
javac -classpath /path/to/jahmm-<version>.jar Myprogram.java
```
...to compile your program, and:
```
java -cp /path/to/jahmm-<version>.jar myMainClass
```
(e.g. `java -cp /home/smith/java_class/jahmm-0.6.2.jar test/Testing`)

...to run it.
You can also put the '.jar' file in your classpath.



## Testing

Once the library has been compiled, you can launch a sample program by typing:
```
mvn -Psample compile
```
(if you use maven)

or

```
ant sample
```
(if you use ant)

...in the distribution root directory.  This launches the `SimpleExample.java`
sample program.

Regression (JUnit) tests have also been written ; see `build.xml/pom.xml` and the
`src/test/java/be/ac/ulg/montefiore/run/jahmm/test` directory.  To launch those tests,
use `ant junit` or `mvn test`.


## Organization

- pom.xml: the 'maven' project file.
- build.xml: the 'ant' build file.
- src/main/java:       all the .java files.
  src/main/.../distributions: Pseudo random distributions.
  src/main/.../jahmm: The jahmm library itself.  This directory holds one
             directory per java package; see the jahmm website for
             more information about each of them.
  src/test/: Regression tests.
  src/main/.../jahmm/apps: Simple applications.
- examples: various example files
- README: this file.
- CHANGES: changelog.
- LICENSE: license file.
- THANKS: contributors.


## Contact

Jahmm's author is Jean-Marc François.  
Feel free to send comments and questions related to this library at:
* http://groups.google.com/group/jahmm-discuss or `jahmm-discuss@googlegroups.com`
  (for questions/comments)
