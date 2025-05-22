pipeline {
    agent any

    tools {
        maven 'my-maven'
    }

    environment {
        BRANCH_NAME = "${env.BRANCH_NAME}"
    }

    stages {
        stage('Build') {
            steps {
                echo "Running build for branch: ${BRANCH_NAME}"
                bat 'mvn clean compile'
            }
        }
    }

    post {
        always {
            echo "Build stage completed for branch: ${BRANCH_NAME}"
        }
    }
}
