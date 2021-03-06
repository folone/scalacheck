# A simple ScalaCheck sbt project

This is a minimal project with a single test that is meant to be used to
quickly get started with ScalaCheck.

The project can be built with [sbt](http://www.scala-sbt.org/). Follow the
instructions on
[http://www.scala-sbt.org/release/docs/Getting-Started/Setup.html] to get
started. sbt is easy to set up on Windows, Mac and Linux, and its only
requirement is a working Java installation of version 1.6 or later.

When you have installed sbt and made it available in your path, you should
replicate this project on your computer. You can do it by manually setting up
the directory structure and file contents, or by downloading the complete
ScalaCheck repository.

To then test the ScalaCheck properties with sbt, run the command `sbt test` in
the root directory of the project (the directory where the file `build.sbt` is
located):

    examples/simple-sbt $ sbt test
    Getting net.java.dev.jna jna 3.2.3 ...
    downloading http://repo1.maven.org/maven2/net/java/dev/jna/jna/3.2.3/jna-3.2.3.jar ...
    	[SUCCESSFUL ] net.java.dev.jna#jna;3.2.3!jna.jar (231ms)
    :: retrieving :: org.scala-sbt#boot-jna
    	confs: [default]
    	1 artifacts copied, 0 already retrieved (838kB/30ms)
    Getting org.scala-sbt sbt 0.12.3 ...
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/sbt/0.12.3/jars/sbt.jar ...
    	[SUCCESSFUL ] org.scala-sbt#sbt;0.12.3!sbt.jar (923ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/main/0.12.3/jars/main.jar ...
    	[SUCCESSFUL ] org.scala-sbt#main;0.12.3!main.jar (4219ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/compiler-interface/0.12.3/jars/compiler-interface-src.jar ...
    	[SUCCESSFUL ] org.scala-sbt#compiler-interface;0.12.3!compiler-interface-src.jar (789ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/compiler-interface/0.12.3/jars/compiler-interface-bin.jar ...
    	[SUCCESSFUL ] org.scala-sbt#compiler-interface;0.12.3!compiler-interface-bin.jar (941ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/precompiled-2_8_2/0.12.3/jars/compiler-interface-bin.jar ...
    	[SUCCESSFUL ] org.scala-sbt#precompiled-2_8_2;0.12.3!compiler-interface-bin.jar (929ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/precompiled-2_9_3/0.12.3/jars/compiler-interface-bin.jar ...
    	[SUCCESSFUL ] org.scala-sbt#precompiled-2_9_3;0.12.3!compiler-interface-bin.jar (917ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/precompiled-2_10_1/0.12.3/jars/compiler-interface-bin.jar ...
    	[SUCCESSFUL ] org.scala-sbt#precompiled-2_10_1;0.12.3!compiler-interface-bin.jar (914ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/actions/0.12.3/jars/actions.jar ...
    	[SUCCESSFUL ] org.scala-sbt#actions;0.12.3!actions.jar (1161ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/interface/0.12.3/jars/interface.jar ...
    	[SUCCESSFUL ] org.scala-sbt#interface;0.12.3!interface.jar (792ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/io/0.12.3/jars/io.jar ...
    	[SUCCESSFUL ] org.scala-sbt#io;0.12.3!io.jar (1085ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/ivy/0.12.3/jars/ivy.jar ...
    	[SUCCESSFUL ] org.scala-sbt#ivy;0.12.3!ivy.jar (1322ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/launcher-interface/0.12.3/jars/launcher-interface.jar ...
    	[SUCCESSFUL ] org.scala-sbt#launcher-interface;0.12.3!launcher-interface.jar (843ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/logging/0.12.3/jars/logging.jar ...
    	[SUCCESSFUL ] org.scala-sbt#logging;0.12.3!logging.jar (793ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/process/0.12.3/jars/process.jar ...
    	[SUCCESSFUL ] org.scala-sbt#process;0.12.3!process.jar (809ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/run/0.12.3/jars/run.jar ...
    	[SUCCESSFUL ] org.scala-sbt#run;0.12.3!run.jar (788ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/command/0.12.3/jars/command.jar ...
    	[SUCCESSFUL ] org.scala-sbt#command;0.12.3!command.jar (915ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/classpath/0.12.3/jars/classpath.jar ...
    	[SUCCESSFUL ] org.scala-sbt#classpath;0.12.3!classpath.jar (785ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/completion/0.12.3/jars/completion.jar ...
    	[SUCCESSFUL ] org.scala-sbt#completion;0.12.3!completion.jar (915ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/api/0.12.3/jars/api.jar ...
    	[SUCCESSFUL ] org.scala-sbt#api;0.12.3!api.jar (938ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/compiler-integration/0.12.3/jars/compiler-integration.jar ...
    	[SUCCESSFUL ] org.scala-sbt#compiler-integration;0.12.3!compiler-integration.jar (809ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/compiler-ivy-integration/0.12.3/jars/compiler-ivy-integration.jar ...
    	[SUCCESSFUL ] org.scala-sbt#compiler-ivy-integration;0.12.3!compiler-ivy-integration.jar (789ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/task-system/0.12.3/jars/task-system.jar ...
    	[SUCCESSFUL ] org.scala-sbt#task-system;0.12.3!task-system.jar (806ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/tasks/0.12.3/jars/tasks.jar ...
    	[SUCCESSFUL ] org.scala-sbt#tasks;0.12.3!tasks.jar (789ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/tracking/0.12.3/jars/tracking.jar ...
    	[SUCCESSFUL ] org.scala-sbt#tracking;0.12.3!tracking.jar (799ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/testing/0.12.3/jars/testing.jar ...
    	[SUCCESSFUL ] org.scala-sbt#testing;0.12.3!testing.jar (806ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/control/0.12.3/jars/control.jar ...
    	[SUCCESSFUL ] org.scala-sbt#control;0.12.3!control.jar (804ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/collections/0.12.3/jars/collections.jar ...
    	[SUCCESSFUL ] org.scala-sbt#collections;0.12.3!collections.jar (932ms)
    downloading http://repo1.maven.org/maven2/jline/jline/1.0/jline-1.0.jar ...
    	[SUCCESSFUL ] jline#jline;1.0!jline.jar (238ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/incremental-compiler/0.12.3/jars/incremental-compiler.jar ...
    	[SUCCESSFUL ] org.scala-sbt#incremental-compiler;0.12.3!incremental-compiler.jar (938ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/compile/0.12.3/jars/compile.jar ...
    	[SUCCESSFUL ] org.scala-sbt#compile;0.12.3!compile.jar (941ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/persist/0.12.3/jars/persist.jar ...
    	[SUCCESSFUL ] org.scala-sbt#persist;0.12.3!persist.jar (917ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/classfile/0.12.3/jars/classfile.jar ...
    	[SUCCESSFUL ] org.scala-sbt#classfile;0.12.3!classfile.jar (834ms)
    downloading http://repo1.maven.org/maven2/org/scala-tools/sbinary/sbinary_2.9.0/0.4.0/sbinary_2.9.0-0.4.0.jar ...
    	[SUCCESSFUL ] org.scala-tools.sbinary#sbinary_2.9.0;0.4.0!sbinary_2.9.0.jar (134ms)
    downloading http://repo1.maven.org/maven2/org/apache/ivy/ivy/2.3.0-rc1/ivy-2.3.0-rc1.jar ...
    	[SUCCESSFUL ] org.apache.ivy#ivy;2.3.0-rc1!ivy.jar (264ms)
    downloading http://repo1.maven.org/maven2/com/jcraft/jsch/0.1.46/jsch-0.1.46.jar ...
    	[SUCCESSFUL ] com.jcraft#jsch;0.1.46!jsch.jar (71ms)
    downloading http://repo1.maven.org/maven2/commons-httpclient/commons-httpclient/3.1/commons-httpclient-3.1.jar ...
    	[SUCCESSFUL ] commons-httpclient#commons-httpclient;3.1!commons-httpclient.jar (74ms)
    downloading http://repo1.maven.org/maven2/commons-logging/commons-logging/1.0.4/commons-logging-1.0.4.jar ...
    	[SUCCESSFUL ] commons-logging#commons-logging;1.0.4!commons-logging.jar (56ms)
    downloading http://repo1.maven.org/maven2/commons-codec/commons-codec/1.2/commons-codec-1.2.jar ...
    	[SUCCESSFUL ] commons-codec#commons-codec;1.2!commons-codec.jar (56ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/cache/0.12.3/jars/cache.jar ...
    	[SUCCESSFUL ] org.scala-sbt#cache;0.12.3!cache.jar (1170ms)
    downloading http://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/test-agent/0.12.3/jars/test-agent.jar ...
    	[SUCCESSFUL ] org.scala-sbt#test-agent;0.12.3!test-agent.jar (792ms)
    downloading http://repo1.maven.org/maven2/org/scala-tools/testing/test-interface/0.5/test-interface-0.5.jar ...
    	[SUCCESSFUL ] org.scala-tools.testing#test-interface;0.5!test-interface.jar (55ms)
    :: retrieving :: org.scala-sbt#boot-app
    	confs: [default]
    	41 artifacts copied, 0 already retrieved (8574kB/32ms)
    Getting Scala 2.9.2 (for sbt)...
    downloading http://repo1.maven.org/maven2/org/scala-lang/scala-compiler/2.9.2/scala-compiler-2.9.2.jar ...
    	[SUCCESSFUL ] org.scala-lang#scala-compiler;2.9.2!scala-compiler.jar (478ms)
    downloading http://repo1.maven.org/maven2/org/scala-lang/scala-library/2.9.2/scala-library-2.9.2.jar ...
    	[SUCCESSFUL ] org.scala-lang#scala-library;2.9.2!scala-library.jar (224ms)
    downloading http://repo1.maven.org/maven2/org/scala-lang/jline/2.9.2/jline-2.9.2.jar ...
    	[SUCCESSFUL ] org.scala-lang#jline;2.9.2!jline.jar (134ms)
    downloading http://repo1.maven.org/maven2/org/fusesource/jansi/jansi/1.4/jansi-1.4.jar ...
    	[SUCCESSFUL ] org.fusesource.jansi#jansi;1.4!jansi.jar (57ms)
    :: retrieving :: org.scala-sbt#boot-scala
    	confs: [default]
    	4 artifacts copied, 0 already retrieved (20090kB/24ms)
    [info] Set current project to scalacheck-demo (in build file:/home/rickard/wrk/personal/scalacheck/examples/simple-sbt/)
    Getting Scala 2.10.1 ...
    downloading http://repo1.maven.org/maven2/org/scala-lang/scala-compiler/2.10.1/scala-compiler-2.10.1.jar ...
    	[SUCCESSFUL ] org.scala-lang#scala-compiler;2.10.1!scala-compiler.jar (602ms)
    downloading http://repo1.maven.org/maven2/org/scala-lang/scala-library/2.10.1/scala-library-2.10.1.jar ...
    	[SUCCESSFUL ] org.scala-lang#scala-library;2.10.1!scala-library.jar (312ms)
    downloading http://repo1.maven.org/maven2/org/scala-lang/scala-reflect/2.10.1/scala-reflect-2.10.1.jar ...
    	[SUCCESSFUL ] org.scala-lang#scala-reflect;2.10.1!scala-reflect.jar (208ms)
    downloading http://repo1.maven.org/maven2/org/scala-lang/jline/2.10.1/jline-2.10.1.jar ...
    	[SUCCESSFUL ] org.scala-lang#jline;2.10.1!jline.jar (147ms)
    :: retrieving :: org.scala-sbt#boot-scala
    	confs: [default]
    	5 artifacts copied, 0 already retrieved (24386kB/28ms)
    [info] Updating {file:/home/rickard/wrk/personal/scalacheck/examples/simple-sbt/}default-0b48a9...
    [info] Resolving org.scala-lang#scala-actors;2.10.1 ...
    [info] downloading http://repo1.maven.org/maven2/org/scalacheck/scalacheck_2.10/1.10.1/scalacheck_2.10-1.10.1.jar ...
    [info] 	[SUCCESSFUL ] org.scalacheck#scalacheck_2.10;1.10.1!scalacheck_2.10.jar (143ms)
    [info] downloading http://repo1.maven.org/maven2/org/scala-lang/scala-actors/2.10.1/scala-actors-2.10.1.jar ...
    [info] 	[SUCCESSFUL ] org.scala-lang#scala-actors;2.10.1!scala-actors.jar (115ms)
    [info] Done updating.
    [info] Compiling 1 Scala source to /home/rickard/wrk/personal/scalacheck/examples/simple-sbt/target/scala-2.10/test-classes...
    [info] + Demo.myprop: OK, passed 100 tests.
    [info] Passed: : Total 1, Failed 0, Errors 0, Passed 1, Skipped 0
    [success] Total time: 10 s, completed May 23, 2013 8:09:01 AM


sbt will automatically download all needed dependencies. The output from the
above command might look differently if you already have some or all
dependencies installed or cached.

The last three lines of the output is what you should look for in your own
output. It tells us that the property `Demo.myprop` passed 100 evaluations, and
then gives a summary of the results (in this case, there's only one property,
so the summary is not that interesting).

Now you can go ahead and experiment by modifying the existing property or
adding new ones. sbt will pick up any Scala file that contains ScalaCheck
properties, if it is located somewhere under `src/test/scala`. Look at the
existing file `src/test/scala/Demo.scala` for inspiration.
