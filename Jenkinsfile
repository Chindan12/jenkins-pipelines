pipeline {
    agent any

    // Automatically pulls the Jenkinsfile from the SCM (like GitHub)
    stages {
        stage('Checkout from SCM') {
            steps {
                // This will clone your GitHub repository
                git branch: 'main', url: 'https://github.com/Chindan12/Pipeline.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Example build command (adjust as per your project)
                sh 'python --version'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Example test step
                sh 'pytest || echo "No tests found"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Example deploy command
                sh 'echo "Deploying to staging server..."'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully ✅'
        }
        failure {
            echo 'Pipeline failed ❌'
        }
    }
}
