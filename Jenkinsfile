pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    
    stages {
        stage('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Mounika12787189/bookstore.git']]])
            }
        }
        stage ('Build'){
            steps {
                sh 'mvn clean package'
            }
        }
               
                
