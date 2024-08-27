pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build the code using a build automation tool.'
                echo 'Tool: Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Run unit tests and integration tests.'
                echo 'Tool: JUnit for unit tests.'
                echo 'Tool: Selenium foor integration tests.'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyze the code to ensure it meets industry standards.'
                echo 'Tool: SonarQube'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Perform a security scan to identify vulnerabilities.'
                echo 'Tool: OWASP ZAP'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploy the application to a staging server.'
                echo 'Staging Server: AWS EC2 instance'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Run integration tests on the staging environment.'
                echo 'Tool: Selenium'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploy the application to a production server.'
                echo 'Production Server: AWS EC2 instance'
            }
        }
    }

    post {
        success {
            emailext(
                from: 'tamlac20121996@gmail.com',
                to: 'tamlac20121996@gmail.com',
                subject: "Build Successful: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
                body: "This is a simple test message."
            )
        }
        failure {
            emailext(
                from: 'tamlac20121996@gmail.com',
                to: 'tamlac20121996@gmail.com',
                subject: "Build Failed: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
                body: "This is a simple test message."
            )
        }
    }
}