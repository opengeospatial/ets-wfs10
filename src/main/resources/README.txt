
The WFS 1.0 test suite requires the supporting libraries listed below. 

* cite1-utils-1.1.0.jar
  <https://svn.opengeospatial.org/ogc-projects/cite/maven/org/opengis/cite/cite1-utils/>

* gml2-validator-1.1.jar
  <https://svn.opengeospatial.org/ogc-projects/cite/maven/com/galdosinc/gml/gml2-validator/>
  
* jaxen-1.0-FCS.jar
  <http://search.maven.org/remotecontent?filepath=jaxen/jaxen/1.0-FCS/jaxen-1.0-FCS.jar>

* saxpath-1.0-FCS.jar
  <http://search.maven.org/remotecontent?filepath=saxpath/saxpath/1.0-FCS/saxpath-1.0-FCS.jar>


These libraries are included in the ets-resources archive. It may be assembled (using Maven 3.0) 
by executing the 'mvn package' phase; the project may be checked out from the OGC Subversion 
repository at this location:

<https://svn.opengeospatial.org/ogc-projects/cite/ets/ets-resources/trunk>


If you are using the command-line interface, put the JAR files in TE_BASE/resources/lib/.
Otherwise put them in the web app lib directory (WEB-INF/lib/).
