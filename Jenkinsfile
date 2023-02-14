pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ ./main/helo.cpp -o PES1UG21CS824'
                build job: 'PES1UG21CS824-1'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG21CS824'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deployment stage"'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
