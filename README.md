custom-javalangclassloader-class
================================

yet another repository to fiddle with classloaders / native libs management in geOrchestra. The idea behind this project is to circumvent GeoTools issues in the way native libraries are loaded in case of multiple classloaders. See 
https://github.com/geotools/geotools/pull/443 for more info about the motivation.


Compilation
==============

```
$ mvn clean package
```

Usage
=========

Add the following to your `bin/setenv.sh` of your tomcat:

```
export CATALINA_OPTS="${CATALINA_OPTS}  \
  -Xbootclasspath/p:/path/to/your/georchestra-custom-classloader-1.0.jar"

```

