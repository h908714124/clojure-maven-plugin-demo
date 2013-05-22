clojure-maven-plugin-demo
=========================

This is a demonstration of <a href="https://github.com/talios/clojure-maven-plugin/issues/68">a potential bug in clojure-maven-plugin</a>, version 1.3.15. Changing packaging type from ``<packaging>jar</packaging>`` to ``<packaging>clojure</packaging>`` breaks the build of a regular java project: The test resources are not copied from src/test/resources to classes/test-resources anymore.

### Reproduce

Try 

``mvn clean test``

an observe that the build fails, due to test failure. Now change the packaging to ``<packaging>jar</packaging>`` in the pom.xml, and repeat. This time, the test will pass.