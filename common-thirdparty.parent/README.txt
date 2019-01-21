Common Maven Commands
---------------------

Because the parent is meant as a holder of commands for children, install/deployment of the parent itself is a bit different since we don't want the
commands intended for the children to be used.

To locally install the common-thirdparty.parent:

mvn -Ddeploy=self clean install

To deploy the common-thirdparty.parent:

mvn -Djenkins=true -Ddeploy=self clean deploy

To locally install a child project:

mvn clean install

To deploy a child project:

mvn -Djenkins=true -Pdefault clean deploy
