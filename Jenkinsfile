pipeline {
   agent {
        node {
            label 'maven'
        }
   }
   environment {
        PATH = "/usr/bin/mvn/bin:$PATH"
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