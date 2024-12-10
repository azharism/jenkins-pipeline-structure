# jenkins-pipeline-structure--groovy structure\\

pipeline {
    agent { label 'slave-1' }

    tools {
        maven 'Maven 3.8.1' // Specify your Maven version here
        jdk 'JDK 17'        // Specify your JDK version here
    }

    stages {
        stage('Greet 1') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Greet 2') {
            steps {
                echo 'Hello Again'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'mvn clean install' // Example Maven build step
            }
        }
         stage('Greet 2') {
            steps {
                echo 'Hello Again'
            }
        }
    }
}
