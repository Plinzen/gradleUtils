# gradleUtils
Providing some useful utilities for android gradle development.

# javadoc.gradle
Provides the possibility to generate Javadoc with gradle task: generate$Variant$Javadoc. Output folder is /build/outputs/javadoc/$Variant$

## Installation
add the following line to your app build.grade: `https://raw.githubusercontent.com/Plinzen/gradleUtils/master/javadoc.gradle`

# countGitCommits.gradle
Provides a function to count the git commits in your project. Sample usage:

```
def numberOfCommits = countGitCommits();
versionCode 8000 + numberOfCommits
versionName "0.8.$numberOfCommits"
```

## Installation
add the following line to your app build.grade: `https://raw.githubusercontent.com/Plinzen/gradleUtils/master/countGitCommits.gradle`


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
2. add the following line to your app build.grade: `apply from: 'https://raw.githubusercontent.com/Plinzen/gradleUtils/master/checkstyle.gradle'`

## Usage
Run the gradle-tasks checkstyle or checkstyleReport: `./gradlew checkstyle checkstyleReport`

## On-the-Fly usage
Android Studio has an additional plugin `CheckStyle-IDEA` which can be installed and configured to use the rules from the config-folder. The plugin add a new window in the buttombar which shows all checkstyle warnings in the current scope.
