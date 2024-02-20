# **1. Overview**

In this article, we’ll have a quick look at one of the major pieces of new functionality that Java 8 had added – Streams.

We’ll explain what streams are about and showcase the creation and basic stream operations with simple examples.


# **2. Stream API**

One of the major new features in Java 8 is the introduction of the stream functionality – [java.util.stream](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/stream/package-summary.html) – which contains classes for processing sequences of elements.

The central API class is the [Stream<T>](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/stream/Stream.html). The following section will demonstrate how streams can be created using the existing data-provider sources.

## **2.1. Stream Creation**

Streams can be created from different element sources e.g. collections or arrays with the help of stream() and of() methods:

~~~Java
String[] arr = new String[]{"a", "b", "c"};
Stream<String> stream = Arrays.stream(arr);
stream = Stream.of("a", "b", "c");
~~~

A stream() default method is added to the Collection interface and allows creating a Stream<T> using any collection as an element source:

~~~Java
Stream<String> stream = list.stream();
~~~