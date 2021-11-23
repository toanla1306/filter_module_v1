pipeline {
  agent any
  
  tools {
    gradle 'Gradle'
  }
  
  stages {
    stage("run frontend") {
      steps {
        echo 'executing yarn...'
        nodejs('Node-17.1') {
          sh 'yarn install'
        }
      }
    }
    stage("run backend"){
      steps {
        echo 'executing gradle...'
        sh 'chmod +x ./gradlew'
        sh './gradlew -v'
      }
    }
  } 
}
