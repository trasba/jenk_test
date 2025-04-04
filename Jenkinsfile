pipeline {
    agent {
        docker {
            image 'alpine/git' // A small image with Git
            args '-v /var/run/docker.sock:/var/run/docker.sock'
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
        stage('Demo Task with Delay') {
            steps {
                echo 'Starting demo task...'
                sh 'sleep 8' // Introduce an 8-second delay
                echo 'Demo task finished.'
            }
        }
    }
}
