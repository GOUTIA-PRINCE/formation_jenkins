// My first pipeline
pipeline {
    agent any
    stages {
        stage("Hello") {
            steps {
                echo "Hello World"
                echo "bonjour le monde!"
            }
        }
        stage("Informations Systeme") {
            steps {
                sh "date"
                sh "whoami"
                sh "pwd"
            }
        }
    }
}