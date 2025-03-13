pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS507-1'
                sh '''
                    g++ sarahs.cpp -o output
                    echo "Build Stage Successful"
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                    ./output
                    exit 1
                    echo "Test Stage Successful"
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment Successful"
        
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed"
        }
    }
}
