pipeline {
   agent {
        node {
            label 'maven'
        }
   }
   environment {
        PATH = "/opt/apache-maven-3.9.4/bin:$PATH"
   }
    stages {
          stage('Build') {
                steps {
                 sh 'mvn clean deploy'
                }
          }
          stage('Test') {
                steps {
                 echo 'Testing..'
                }
          }
          stage('Deploy') {
                steps {
                 echo 'Deploying....'
                }
          }
          stage('Done') {
                steps {
                 echo 'All done!'
                }
          }
    }
}