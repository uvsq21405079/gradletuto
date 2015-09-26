# gradletuto
Un court tutoriel Gradle.

## Première tâche
```
$ gradle tasks
...
$ gradle Hello
:Hello
Hello !

BUILD SUCCESSFUL

Total time: 0.991 secs
```

### Voir aussi
* [Task](https://docs.gradle.org/current/dsl/org.gradle.api.Task.html)

## Dépendances entre tâches
```
$ gradle world
:hello
Hello, :world
world !

BUILD SUCCESSFUL

Total time: 0.989 secs
```

## Construit un projet groovy
```
$ gradle tasks
...
$ gradle build
:compileJava UP-TO-DATE
:compileGroovy
Download https://repo1.maven.org/maven2/org/codehaus/groovy/groovy-all/2.4.5/groovy-all-2.4.5.jar
:processResources UP-TO-DATE
:classes
:jar
:assemble
:compileTestJava UP-TO-DATE
:compileTestGroovy UP-TO-DATE
:processTestResources UP-TO-DATE
:testClasses UP-TO-DATE
:test UP-TO-DATE
:check UP-TO-DATE
:build

BUILD SUCCESSFUL

Total time: 1 mins 10.772 secs
$ ls build/libs
gradletuto.jar
$ java -cp $GROOVY_HOME/lib/groovy-2.4.5.jar:build/libs/gradletuto.jar fr.uvsq.doosa.gradletuto.Main
Hello
```

### Voir aussi
* Plugin [Groovy](https://docs.gradle.org/current/userguide/groovy_plugin.html)
* Plugin [Java](https://docs.gradle.org/current/userguide/java_plugin.html)
* [repositories](https://docs.gradle.org/current/dsl/org.gradle.api.Project.html#org.gradle.api.Project:repositories%28groovy.lang.Closure%29)
* [dependencies](https://docs.gradle.org/current/dsl/org.gradle.api.Project.html#org.gradle.api.Project:dependencies%28groovy.lang.Closure%29)

## Lancer l'application
```
$ gradle run
:compileJava UP-TO-DATE
:compileGroovy UP-TO-DATE
:processResources UP-TO-DATE
:classes UP-TO-DATE
:run
Hello

BUILD SUCCESSFUL

Total time: 1.663 secs
```

### Voir aussi
* Plugin [application](https://docs.gradle.org/current/userguide/application_plugin.html)
