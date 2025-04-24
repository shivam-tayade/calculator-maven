pipeline {
    agent any

    tools {
        // Define JDK and Maven versions if installed
        jdk 'JDK 11'
        maven 'Maven 3.9.9'
    }

    environment {
        MAVEN_HOME = tool name: 'Maven 3.9.9', type: 'Maven'
        PATH = "${MAVEN_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/shivam-tayade/jenkins-calculator-maven.git'
            }
        }

        stage('Build') {
            steps {
                script {
                    // Clean and build the project
                    sh 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run unit tests
                    sh 'mvn test'
                }
            }
        }

        stage('Deploy') {
            steps {
                // If you want to deploy, add the deploy steps here
                echo 'Deploying...'
            }
        }
    }

    post {
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
