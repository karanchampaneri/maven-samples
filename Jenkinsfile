pipeline {
  agent any

  tools {
    jdk 'DHT_SENSE'
    maven 'DHT_MVN'
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/karanchampaneri/maven-samples.git', branch: 'q2-blueocean')
      }
    }

    stage('run') {
      steps {
        sh 'mvn clean test verify'
      }
    }

  }
}