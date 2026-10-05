//My first pipeline
pipeline {
    agent any
    Stages {
        stage("Hello") {
            steps {
                echo "Hello World"
            }
            steps {
                echo "bonjour le monde!"
            }
        }
        stage("Informations Systeme"){
            steps {
                sh "date"
                sh "whoami"
                sh "pwd"
            }
        }
    }