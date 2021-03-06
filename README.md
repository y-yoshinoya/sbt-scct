#### This is a sbt 0.11.3 plugin for [scct](http://mtkopone.github.com/scct/) the scala code coverage tool.

scct ist auto-installed depending on the scalaVersion of the project.

#### Commands:

* coverage:compile
* coverage:test
* coverage:doc

coverage:test and coverage:doc do the same, so that if you run coverage:package-doc, you get your coverage report packaged.

docDirectory is reused for the coverage report directory

#### Compiling from Source

1. retrive the sources from github:

	git clone git@github.com:y-yoshinoya/sbt-scct.git

2. set sbt version in sbt-scct/project/build.properties:

	sbt.version=0.11.3

3. publish plugin:

	cd sbt-scct
	sbt publish-local

4. add plugin dependency in .sbt/project/plugins/build.sbt:

	libraryDependencies += "ch.craven" %% "scct-plugin" % "0.2"
	
5. to enable ScctPlugin in your project, add the following line to your build.sbt

	seq(ScctPlugin.scctSettings: _*)
