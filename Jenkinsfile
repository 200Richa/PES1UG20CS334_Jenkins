pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ lolo.cpp -o hello'
                build 'PES1UG20CS334-1'
            }
        }
        stage('Test') {
            steps {
                sh './hello'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deployement Successfull"
            }
        }
    }
    
    post {
        failure {
            echo "Pipeline failed"
        }
    }
}
