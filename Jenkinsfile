pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Le code vient d etre recupere depuis GitHub'
            }
        }

        stage('Build') {
            steps {
                echo 'Preparation du dossier de build...'
                sh 'mkdir -p build'
                sh 'cp site/index.html build/'
                sh 'cp site/style.css build/'
                sh 'ls -la build/'
            }
        }

        stage('Test') {
            steps {
                echo 'Verification que les fichiers existent bien...'
                sh 'test -f build/index.html && echo "OK : index.html present"'
                sh 'test -f build/style.css && echo "OK : style.css present"'
            }
        }

        stage('Archive') {
            steps {
                echo 'Archivage du resultat du build...'
                archiveArtifacts artifacts: 'build/**', fingerprint: true
            }
        }
    }
}