#!/usr/bin/env groovy

node {
    def app

    stage('Clone Repository') {
        checkout scm
    }
    stage('Build Image') {
        app = docker.build('bryanbcruz/hello-world-spring-boot')
    }
}

// pipeline {
//     agent any

//     stages {
//         stage('Clone Repository'){
//             steps {
//                 checkout scm
//             }
//         }
//         stage('Build Image'){
//             steps {
//                 docker.build('bryanbcruz/hello-world-spring-boot')
//             }
//         }
//         stage('Build') {
//             steps {
//                 // ./gradlew build
//                 echo 'Building'
//             }
//         }
//         stage('Test') {
//             steps {
//                 echo 'Testing..'
//             }
//         }
//         stage('Deploy') {
//             steps {
//                 echo 'Deploying....'
//             }
//         }
//     }
// }