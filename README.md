# Hello World - Projet Java Simple

## Structure du projet

```
hello-world/
├── pom.xml
├── Jenkinsfile
└── src/
    └── main/
        └── java/
            └── com/
                └── example/
                    └── Main.java
```

## Exécuter le projet

### Avec Maven
```bash
mvn clean compile
mvn package
java -cp target/hello-world-1.0.jar com.example.Main
```

### Ou directement avec Maven
```bash
mvn compile exec:java -Dexec.mainClass="com.example.Main"
```

## Dans IntelliJ IDEA

1. Ouvrir le projet
2. Attendre que Maven synchronise
3. Clic droit sur `Main.java` → Run 'Main.main()'

## Jenkins

Le Jenkinsfile contient un pipeline simple avec 3 étapes :
- Build : Compilation du code
- Package : Création du JAR
- Run : Exécution du Hello World