clojure-maven-plugin-demo
=========================

This is a demonstration of <a href="https://github.com/talios/clojure-maven-plugin/issues/68">a potential bug in clojure-maven-plugin</a>, version 1.3.15. Changing packaging type from ``<packaging>jar</packaging>`` to ``<packaging>clojure</packaging>`` breaks the build of a regular java project: The test resources are not copied from src/test/resources to classes/test-resources anymore.

## Is it a bug, or am I doing it wrong?

Try 

``mvn clean test``

then try it again after the packaging type to jar. 
