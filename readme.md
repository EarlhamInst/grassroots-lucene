# Grassroots Lucene module

[Lucene](https://lucene.apache.org/) is a Java library which provides excellent indexing and
 search features allowing for functionality such as hit highlighting and faceting, 
It is used to provide the functionality of the Grassroots search service and the indexing 
of all services and their associated content. Since this code is Java-based, we don't have 
platform-specific builds. 

This module can either use Solr or interface directly to Lucene using tehir APIs. Both of these 
can be installed and configured manually or you can use the `install_dependencies` script from the 
[build tools](https://github.com/TGAC/grassroots-build-tools) repository

## Building the module

To build the module, we need to specify where we have Lucene and Solr installed as well as their
versions. This is done from a file called `grassroots-lucene.properties`. You can create this 
file by basing it upon the `example-grassroots-lucene.properties` file that is part of this 
repository. Once you have done this, the content will look something like

~~~properties
# The version of lucene installed
lucene.version=8.1.1

# The version of solr installed
solr.version=8.1.1

# The directory where lucene is installed 
lucene.dir=/home/billy/Applications/lucene

# The directory where solr is installed
solr.dir=/home/billy/Applications/solr

# The directory where the grassroots lucene jars, index and taxonomy are installed
install.dir=/home/billy/Applications/grassroots/grassroots/lucene
~~~

which needs to be edited to set these five variables to match the Lucene and Solr installations.

Once these are set, the Grassroots Lucene module can be built using the given Makefile by running

```make all```

and then 

```make install``` to install the Grassroots Lucene libraries into your Grassroots installation.






 
