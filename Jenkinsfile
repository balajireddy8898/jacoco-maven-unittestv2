pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/Ajayvarma8142/jacoco-maven-unittestv2.git', branch: 'master')
      }
    }
    stage('Build') {
      steps {
        bat 'mvn install'
      }
    }
    stage('SonarQube') {
      steps {
        bat 'mvn sonar:sonar'
      }
    }
  }
}