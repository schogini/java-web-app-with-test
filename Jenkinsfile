pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Test') {
      steps {
        sh 'sudo mvn  test'
      }
    }
    stage('Build') {
      steps {
        sh 'sudo mvn package'
      }
    }
    stage('Deploy') {
      steps {
        sh '''sudo cp -p ./target/SampleJava1.war /var/lib/tomcat8/webapps/sree-bo2.war
'''
        sh 'sudo rm -fr *'
      }
    }
  }
}