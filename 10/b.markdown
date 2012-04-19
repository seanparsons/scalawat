SBT Basics
==========

SBT is run similarly to [Ant](http://ant.apache.org/) or [Maven](http://maven.apache.org/) via a series of commands that you add on the end of the command line:

```
\$ sbt clean
[info] Loading global plugins from /Users/Sean/.sbt/plugins
[info] Set current project to default-66315d (in build file:/Users/Sean/test/)
[success] Total time: 0 s, completed Feb 15, 2012 12:24:21 PM
```

SBT also supports being run interactively if no commands are specified:

```
\$ sbt
[info] Loading global plugins from /Users/Sean/.sbt/plugins
[info] Set current project to default-66315d (in build file:/Users/Sean/test/)
> clean
[success] Total time: 0 s, completed Feb 15, 2012 12:25:07 PM
>
```

