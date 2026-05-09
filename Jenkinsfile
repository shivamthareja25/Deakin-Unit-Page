pipeline {
    agent any

    environment {
        DIRECTORY_PATH = '/Users/shivamthareja/Desktop/Deakin-Unit-Page'
        TESTING_ENVIRONMENT = 'staging'
        PRODUCTION_ENVIRONMENT = 'Shivam Thareja'
    }

    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory path specified by the environment variable"
                echo "Compile the code and generate any necessary artefacts"
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
                echo "Deploy the application to a testing environment specified by the environment variable"
            }
        }

        stage('Approval') {
            steps {
                sleep(time: 10, unit: 'SECONDS')
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying the application to production environment: ${PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
