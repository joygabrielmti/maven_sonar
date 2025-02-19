pipeline {
  agent none
  tools {
    maven 'mvn'
  }
  stages {
    stage("build & sonarqube") {
      agent any
      steps {
        withSonarQubeEnv('sonar-scanner') {
          sh 'mvn clean package sonar:sonar'
        }
      }
    }
  }
}
