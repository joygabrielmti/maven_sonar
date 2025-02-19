     pipeline {
        agent none
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
