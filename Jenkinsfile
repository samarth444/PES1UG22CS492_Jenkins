pipeline {
    agent any // Run on any available node (or agent)

    stages {
        // Build Stage: Compile hello.cpp
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o main/hello_exec'
            }
        }

        // Test Stage: Execute the compiled file
        stage('Test') {
            steps {
                sh './main/hello_exec'
            }
        }

        // Deploy Stage: Simulate deployment (mock)
        stage('Deploy') {
            steps {
                echo 'Deployment Successful: Simulating Deployment...'
            }
        }
    }

    // Handle post-build conditions (success/failure)
    post {
        success {
            echo '✅ Pipeline executed successfully!'
        }
        failure {
            echo '❌ Pipeline failed. Check logs for errors.'
        }
    }
}
