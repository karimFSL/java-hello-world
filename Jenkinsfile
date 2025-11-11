pipeline {
    agent any

    tools {
        maven 'Maven'
        jdk 'JDK-17'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Compilation...'
                sh 'echo "JAVA_HOME=$JAVA_HOME"'
                sh 'java -version'
                sh 'mvn clean compile'
            }
        }

        stage('Package') {
            steps {
                echo 'Création du JAR...'
                sh 'mvn package'
            }
        }

        stage('Run') {
            steps {
                echo 'Exécution du programme...'
                sh 'java -cp target/hello-world-1.0.jar main.java.com.Main'
            }
        }
    }
}