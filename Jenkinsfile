pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project...'
                    sh 'g++ -o output main.cpp' 
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sh './output' 
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                    sh 'exit 1'
                }
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
