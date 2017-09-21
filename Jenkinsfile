pipeline {
  agent any
  stages {
    stage('Compilar') {
      steps {
        withMaven(maven: 'mvn-3.5.0') {
          sh 'mvn clean package -Dmaven.test.failure.ignore'
        }
        
      }
    }
    stage('Arquivar') {
      steps {
        archiveArtifacts '*.jar'
      }
    }
  }
}