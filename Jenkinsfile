pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    
    stages {
        stage('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/srikanthbathini/bookstore.git']]])
            }
        }
        stage ('Build'){
            steps {
                sh 'mvn clean package'
            }
        }
               
                
