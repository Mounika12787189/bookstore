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
        stage ('Bemailext body: 'Hi welcome to jenkins email alerts', subject: 'email-job', to: 'mounika81234@gmail.com'uild'){
            steps {
                sh 'mvn clean package'
            }
        }
        stage ('Email Notification'){
            steps {
                emailext body: 'Hi welcome to jenkins email alerts', subject: 'email-job', to: 'mounika81234@gmail.com'
            }
        } 
    }  
}             
