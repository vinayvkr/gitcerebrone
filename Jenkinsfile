pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'vinayvkr', url: 'https://github.com/cerebrone-ai/gitcerebrone.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn deploy -DskipTests'
            }
        }
    }
  }
