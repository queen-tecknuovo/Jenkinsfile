pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Build stage started'
                sh 'pwd'
                sh 'ls'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage started'
                sh 'touch testfile.txt'
                sh 'ls'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage started'
                sh 'mkdir -p deploy'
                sh 'mv testfile.txt deploy/'
                sh 'ls deploy'
            }
        }
    }
}
