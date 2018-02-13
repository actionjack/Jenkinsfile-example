#!/usr/bin/env groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Stage...'
                checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                  userRemoteConfigs: [[url: 'https://github.com/blade-samples/hello.git']]])
            }
        }
        stage('Test') {
            steps {
                echo 'Testing Stage...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Stage.'
            }
        }
    }
}
