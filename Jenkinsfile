#!/usr/bin/env groovy
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Building Stage...'
                checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                  userRemoteConfigs: [[url: 'https://github.com/sullis/dropwizard-helloworld.git']]])
            }
        }
        stage('Build') {
            steps {
                sh '''
                    pwd
                    ls
                    mvn clean package
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Stage.'
            }
        }
    }
}
