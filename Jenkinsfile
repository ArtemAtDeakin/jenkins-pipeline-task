pipeline {
    agent any
    environment {
        DIRECTORY_PATH = '/path/to/your/code'
        TESTING_ENVIRONMENT = 'testing'
        PRODUCTION_ENVIRONMENT = 'your-name'
    }
    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory path: ${env.DIRECTORY_PATH}"
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy the application to the testing environment: ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                echo "Waiting for approval"
                sleep(time: 10, unit: 'SECONDS')
                echo "Approval received"
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploy the code to the production environment: ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
