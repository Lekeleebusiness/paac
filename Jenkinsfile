pipeline {
    agent any

    stages {
        stage('SCM Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Lekeleebusiness/paac']]])
            }
        }
        
        stage('Build'){
            steps{
                sh 'mvn install'
            }
        }
        
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
    }
}
