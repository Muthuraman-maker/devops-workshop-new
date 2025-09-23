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
                 sh 'mvn clean install'
                }
          }
          stage('Test') {
                steps {
                 sh 'mvn test'
                }
          }
          stage('Deploy') {
                steps {
                 sh 'mvn deploy'
                }
          }
    }
}