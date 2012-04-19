Java Interop
============

Scala works pretty much interoperably with Java, there are just a couple of things to be careful of.
<br/>
<br/>
Using Java libraries/code in Scala should be pretty much seamless, the only thing that will become a necessity will be the use of the [JavaConverters](http://www.scala-lang.org/api/current/scala/collection/JavaConverters\$.html) object.
<br/>
<br/>
Using Scala libraries/code from Java will potentially necessitate avoiding features of Scala that don't map well to Java, implicit and multiple parameter groups as well as functions will be awkward at best. In this case it would be advised to create additional methods using Scala to shield off these difficulties and provide interfaces that are more Java like.
