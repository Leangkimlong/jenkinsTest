pipeline {
    agent any

    tools {
        gradle 'Gradle87' // Use the correct Gradle tool name
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Leangkimlong/jenkinsTest.git'
            }
        }
        stage('Build') {
            steps {
                sh './gradlew build' // This assumes the Gradle wrapper is present
            }
        }
    }

    post {
        success {
            // Additional steps to perform on successful build
        }
        failure {
            // Additional steps to perform on build failure
        }
    }
}
