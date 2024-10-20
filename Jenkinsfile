pipeline {
    agent any
    triggers {
            githubPush()
        }
    tools {
        maven 'Maven3'
        jdk 'JDK'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/pzsbbfan/COMP367LAB02.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
