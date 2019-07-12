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
    stage('test') {
      steps {
        bat 'mvn test'
      }
    }
    stage('Deploy') {
      steps {
        bat 'cd C:\\Program Files (x86)\\Jenkins\\workspace\\jacoco-maven-unittestv2_master\\target\\ajay  java -jar ajay-1.0.jar'
      }
    }
  }
}