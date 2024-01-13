pipeline {
    agent any

   
    
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Shantanux/project.git']]])
            }
        }
        
        stage('Build jar') {
            steps {
                sh "mvn clean install"
            }
        }
    } }