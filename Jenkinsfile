pipeline {
    agent {
        docker {
            image 'alpine/git' // A small image with Git
        }
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('List Files') {
            steps {
                sh 'ls -l'
            }
        }
    }
}
