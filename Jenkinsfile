pipeline { 
    agent { label 'slave-1'}
    
    tools {
        maven 'maven3'
        jdk 'jdk17'
    }

    stages {
        stage('Git Checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/sraamik/FullStack-Blogging-App.git'
            }
        }
        
        stage('compile') {
            steps {
            sh "mvn compile"
            }
        }
        stage('Test') {
            steps {
            sh "mvn test"
            }
        }
         stage('Package') {
            steps {
            sh "mvn package"
            }
        }
    }
    
}
