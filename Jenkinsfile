pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'cd /var/jenkins_home/workspace/PES2UG22CS180-1/main && g++ hello.cpp -o hello_pipeline'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'cd /var/jenkins_home/workspace/PES2UG22CS180-1/main && ./hello_pipeline'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                echo 'Deployment completed successfully'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
