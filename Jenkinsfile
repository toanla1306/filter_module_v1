pipeline {
  agent any
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
        withGradle('Gradle') {
          sh './gradlew -v'
        }
      }
    }
  } 
}
