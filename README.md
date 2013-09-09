spout-archetype
===============

A Maven ArcheType for Spout Server

The spout-archetype was created to help speed up the process of creating a plugin.

Developers please feel free to contribute to the archetype

What is an Archetype
--------------------
An archetype is basically a template used to help create maven applications. They include:

* Dependencies needed for basic operation (in this case spoutapi)
* Repositories are already filled in (repo.spout.org)
* POMs are already filled in with variables that are assigned when you select the archetype
* Files are already pre-named
* Files and File structures are already in place.
* Basic code to get you started is already done for you.

An archetype is not only for beginner coders, or people new to the project, it is designed to be used by even experienced coders, it does get tedious to always create the base code by hand.

Repository Settings

* ArtifactId = spout-archetype
* Repository = http://repository-tenowg.forge.cloudbees.com/release/
* Version = 1.2
* GroupID = com.thedemgel

Using this Archetype from the Command Line
------------------------------------------
You will need a copy of Maven 2 or 3 installed on your system. You can check if you have one by running `mvn --version` in the command line. Now, navigate to the directory you would like to place your project in and run

	mvn archetype:generate -DarchetypeArtifactId=spout-archetype                                        \
	                       -DarchetypeGroupId=com.thedemgel                                             \
	                       -DarchetypeVersion=1.2                                                       \
	                       -DarchetypeRepository=http://repository-tenowg.forge.cloudbees.com/release/

After Maven downloads the archetype once, you can omit the `-DarchetypeRepository` flag to use the one on your local system. The archetype will also accept the following flags:

* `-DartifactId` the identifier for your project. For example, this project has the artifactId `spout-archetype`.
* `-DgroupId` by convention, this is the reverse of your web address (i.e. `com.awesomeplugins`), and if you do not have one use `me.yourname`.
* `-Dversion` the version of your plugin.
* `-DpluginName` allows you to specify the name of your plugin (i.e. `BetterMobs`, `ArcheryTools`). Defaults to `-DartifactId`.
* `-Dpackage` allows you to change the package of your main heirarchy. Defaults to `-DgroupId.-DartifactId`.

Note that if you do not specify these flags, Maven will prompt you for them. A more complete example might look like this:

	mvn archetype:generate -DarchetypeArtifactId=spout-archetype                                        \
	                       -DarchetypeGroupId=com.thedemgel                                             \
	                       -DarchetypeVersion=1.1                                                       \
	                       -DarchetypeRepository=http://repository-tenowg.forge.cloudbees.com/release/  \
	                       -DartifactId=test                                                            \
	                       -DgroupId=me.testmaker                                                       \
	                       -Dversion=1.0.0                                                              \
	                       -DpluginName=Test                                                            \
	                       -Dpackage=me.testmaker.plugins.test

Eclipse Tutorial
----------------
TODO: need to add Eclipse tutorial on how to add an archetype

NetBeans Tutorial
-----------------
TODO: need to add NetBeans tutorial on how to add an archetype

Building from Source
--------------------
Assuming you have Maven installed on your system, navigate to the directory you would like to place the source code in and run

	git clone git://github.com/tenowg/spout-archetype.git
	cd spout-archetype
	mvn clean install archetype:update-local-catalog

The archetype is now installed on your local system, and can be accessed in any of the methods outlined above. In particular, you can be sure to use the version in your local system by running `mvn archetype:generate` with the `-DarchetypeCatalog=local` flag.

License
-------
This project is licensed under `The Mit License (MIT)`.