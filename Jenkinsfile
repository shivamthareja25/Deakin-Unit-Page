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
                echo 'Stage 1: Build'
                echo 'Task: Compiling and packaging the application source code.'
                echo 'Tool: Maven – build automation tool used to compile and package Java projects.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests'
                echo 'Task: Running unit tests to validate individual components and integration tests to verify component interactions.'
                echo 'Tool: JUnit for unit tests, Selenium for integration tests.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis'
                echo 'Task: Analysing code to ensure it meets industry standards and best practices.'
                echo 'Tool: SonarQube – static code analysis tool that identifies bugs, code smells, and vulnerabilities.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan'
                echo 'Task: Scanning code and dependencies for known security vulnerabilities (CVEs).'
                echo 'Tool: OWASP Dependency-Check – scans project dependencies against the NVD vulnerability database.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging'
                echo "Task: Deploying application to testing environment: ${TESTING_ENVIRONMENT}"
                echo 'Tool: AWS CLI – deploys to an AWS EC2 staging instance.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging'
                echo 'Task: Running integration tests on the staging environment to validate production-like behaviour.'
                echo 'Tool: Selenium WebDriver – automates browser-based end-to-end tests.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Stage 7: Deploy to Production"
                echo "Task: Deploying the verified application to production environment: ${PRODUCTION_ENVIRONMENT}"
                echo 'Tool: AWS CLI – deploys to an AWS EC2 production instance after all checks pass.'
            }
        }

    }
}
