# gradleUtils
Providing some useful utilities for android gradle development.

# javadoc.gradle
Provides the possibility to generate Javadoc with gradle task: generate$Variant$Javadoc. Output folder is /build/outputs/javadoc/$Variant$

## Installation
add the following line to your app build.grade: `https://raw.githubusercontent.com/Plinzen/gradleUtils/master/javadoc.gradle`

# checkstyle.gradle
Add some Checkstyle code analysis tasks. Works currently only without product flavor usage since some paths are hard coded.

## Installation
1. Copy the config-folder (containing checkstyle.xml and checkstyle.xsl) from the repository to your app-folder within your project. Your file structure should look similar to that:
```
project-root
 |-> app
      |->config
          |-> checkstyle.xml
          |-> checkstyle.xsl
```

2. add the following line to your app build.grade: `https://raw.githubusercontent.com/Plinzen/gradleUtils/master/checkstyle.gradle`
