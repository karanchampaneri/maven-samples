pipeline {
  agent any

  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }

  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/karanchampaneri/maven-samples.git', branch: 'q2-blueocean')
      }
    }

    stage('clean') {
      steps {
        sh 'mvn clean'
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('verify') {
      steps {
        sh 'mvn verify'
      }
    }
  }
}