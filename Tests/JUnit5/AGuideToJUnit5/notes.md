<h1><strong>1. Overview</strong></h1>
<p>JUnit is one of the most popular unit-testing frameworks in the Java ecosystem. The JUnit 5 version contains a number of exciting innovations, with <strong>the goal of supporting new features in Java 8 and above</strong>, as well as enabling many different styles of testing.</p>


<hr>


<h1><strong>2. Maven Dependencies</strong></h1>
<p>Setting up to <strong>JUnit5.x.0</strong> is pretty straightfoward: we just need to add th following dependency to out pom.xml:</p>

~~~
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-engine</artifactId>
    <version>5.9.2</version>
    <scope>test</scope>
</dependency>
~~~

<p>Furthermore, there’s now direct support to run Unit tests on the JUnit Platform in Eclipse, as well as IntelliJ. We can, of course, also run tests using the Maven Test goal.</p>
<p>On the other hand, IntelliJ supports JUnit 5 by default. Therefore, running JUnit 5 on IntelliJ is pretty easy. We simply Right click –> Run, or Ctrl-Shift-F10.</p>
<p>It’s important to note that this version <strong>requires Java 8 to work.</strong></p>


<hr>


<h1><strong></strong></h1>


<hr>


<h1><strong></strong></h1>