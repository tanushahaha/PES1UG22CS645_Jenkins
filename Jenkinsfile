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
                    echo "deploying project...."
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
