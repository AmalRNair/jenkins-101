pipeline {
    agent any
    triggers{
        pollSCM 'H/5 * * * *'
    }
    stages {
        stage('Build') {
            steps {
                // Your build steps go here
                echo 'Building...'
            }
        }

        stage('Test') {
            steps {
                // Your test steps go here
                echo 'Testing...'
                echo 'Testing pollSCM'
            }
        }

        stage('Deploy') {
            steps {
                // Your deployment steps go here
                echo 'Deploying...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! Send notifications, cleanup, etc.'
        }
        failure {
            echo 'Pipeline failed! Send notifications, cleanup, etc.'
        }
    }
}
