#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stage('Clone Repository'){
            steps {
                checkout scm
            }
        }
        stage('Build Image'){
            steps {
                app = docker.build("bryanbcruz/hello-world-spring-boot")
            }
        }
        stage('Build') {
            steps {
                // ./gradlew build
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}