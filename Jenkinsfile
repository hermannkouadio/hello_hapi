#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'bngdocker/update '
            args '-u bngdev'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
    }
}
