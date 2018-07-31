pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'sudo mvn clean'
      }
    }
    stage('Test') {
      steps {
        sh 'sudo mvn  test'
      }
    }
    stage('Deploy') {
      steps {
        sh '''sudo cp -p ./SampleJava1.war /var/lib/tomcat8/webapps/sree-bo2.war
'''
      }
    }
  }
}