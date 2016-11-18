Macker-Original
=================

Fork of the original Macker project.

 * [Original website](https://innig.net/macker/guide/index.html)
 * [Original SourceForge svn-repository](https://sourceforge.net/projects/macker/)

Macker helps enforce architectural rules (layering, tiering, modularity, etc) in your Java code. It applies pattern-based access rules from XML rules files to your compiled classes.


# Getting Started

1. Install [Apache Ant](http://ant.apache.org)
  * [Ant Tutorial for Mac](http://www.mkyong.com/ant/how-to-apache-ant-on-mac-os-x/)

2. Install [Apache Maven](https://maven.apache.org)
 * [Maven Tutorial for Mac](https://www.mkyong.com/maven/install-maven-on-mac-osx/)

3. Clone this repository
 ```bash
git clone git@github.com:Andrej1A/Macker-Original.git
 ```

4. Change to the directory of the basic example
 ```bash
cd macker/doc/example/basic
 ```

5. Execute ant
```bash
ant
```

6. You will seee the following output:

```
Buildfile: /Users/andrej/Documents/workspaceJava2016/Original-Macker-Fork/macker/doc/example/basic/build.xml

prepare:
    [mkdir] Created dir: /Users/andrej/Documents/workspaceJava2016/Original-Macker-Fork/macker/build/example/basic
    [mkdir] Created dir: /Users/andrej/Documents/workspaceJava2016/Original-Macker-Fork/macker/build/example/basic/classes

build-macker-jar:

compile:
    [javac] /Users/andrej/Documents/workspaceJava2016/Original-Macker-Fork/macker/doc/example/build-shared.xml:27: warning: 'includeantruntime' was not set, defaulting to build.sysclasspath=last; set to false for repeatable builds
    [javac] Compiling 1 source file to /Users/andrej/Documents/workspaceJava2016/Original-Macker-Fork/macker/build/example/basic/classes

explain:
     [echo]
     [echo] ________________________________________________________________________________
     [echo]
     [echo] This stupidly simple example disallows references from classes whose names
     [echo] contain "Print" to any Java APIs.  As with most of these examples, the source
     [echo] code contains a few violations of the rules, so you can see what such violations
     [echo] will look like.  Note that Macker picks up several references in this example
     [echo] that aren't immediately obvious.
     [echo]
     [echo] With all of these examples, you can:
     [echo]   * Type "ant" to see macker apply the rules
     [echo]   * Type "ant -Dmacker.verbose=true" to see some details of what's going on
     [echo]   * Edit "src/macker.xml" to fool with different rules
     [echo]   * View an XML report in:
     [echo]     /Users/andrej/Documents/workspaceJava2016/Original-Macker-Fork/macker/build/example/basic/macker-report.xml
     [echo]   
     [echo] Enjoy!
     [echo] ________________________________________________________________________________
     [echo]         

macker:
    [mkdir] Created dir: /Users/andrej/Documents/workspaceJava2016/Original-Macker-Fork/macker/build/example/basic/report
   [macker]
   [macker] (Checking ruleset: Simple example ...)
   [macker]
   [macker] Illegal reference
   [macker]   from PrintHelloWorld
   [macker]     to java.io.PrintStream
   [macker]
   [macker] Illegal reference
   [macker]   from PrintHelloWorld
   [macker]     to java.lang.Object
   [macker]
   [macker] Illegal reference
   [macker]   from PrintHelloWorld
   [macker]     to java.lang.String
   [macker]
   [macker] Illegal reference
   [macker]   from PrintHelloWorld
   [macker]     to java.lang.System
   [macker]
   [macker] (4 errors)
   [macker]
   [macker] Macker rules checking failed

BUILD FAILED
/Users/andrej/Documents/workspaceJava2016/Original-Macker-Fork/macker/doc/example/build-shared.xml:56: Macker rules checking failed

Total time: 1 second
```
