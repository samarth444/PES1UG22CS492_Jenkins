pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ main/invalid_file.cpp -o main/hello_exec' // Intentional error!
            }
        }

        stage('Test') {
            steps {
                sh './main/hello_exec'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Successful: Simulating Deployment...'
            }
        }
    }

    post {
        success {
            echo ' Pipeline executed successfully!'
        }
        failure {
            echo ' Pipeline failed. Check logs for errors.'
        }
    }
}
