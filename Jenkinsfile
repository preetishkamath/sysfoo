pipeline {
  agent any
  stages {
    stage('MAVEN-BUILD') {
      steps {
        sh 'mvn  compile'
      }
    }

    stage('Mavev-Test') {
      steps {
        sh 'mvn clean test'
      }
    }

    stage('Maven-package') {
      steps {
        sh 'mvn package -DskipTests'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/target/*war'
      }
    }

  }
  tools {
    maven 'mavenhome'
  }
}