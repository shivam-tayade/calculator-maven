pipeline {
    agent any

    tools {
        // Use the specific JDK 17 and Maven 3.8.7 versions installed on your system
        jdk 'JDK 17'  // Make sure the JDK name matches what is set in Jenkins under Global Tool Configuration
        maven 'Maven 3.8.7'  // Same for Maven version
    }

    environment {
        MAVEN_HOME = tool name: 'Maven 3.8.7', type: 'Maven'  // This refers to Maven 3.8.7 installed on your Jenkins instance
        PATH = "${MAVEN_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/shivam-tayade/jenkins-calculator-maven.git'  // Your GitHub repository URL
            }
        }

        stage('Build') {
            steps {
                script {
                    // Clean and build the project using Maven
                    sh 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run tests with Maven
                    sh 'mvn test'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add deployment steps if required
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
