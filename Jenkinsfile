pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project'
                echo 'Build successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                echo 'All tests passed'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application'
                echo 'Deployment successful'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
        always {
            echo 'Pipeline finished'
            archiveArtifacts artifacts: '**/*.txt', allowEmptyArchive: true
        }
    }
}
