pipeline {
  agent any

  tools {
    // Gradle wrapper should be present in the project, no need to install explicitly
  }

  stages {
    stage('Clone') {
      steps {
        git branch: 'springs', url: 'https://github.com/Techchhiv/i4jenkins.git'
      }
    }
    stage('Build') {
      steps {
        sh './gradlew build' // This assumes the Gradle wrapper is present
      }
    }
  }
}
