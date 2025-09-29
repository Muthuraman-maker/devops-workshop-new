pipeline {
   agent {
        node {
            label 'maven'
        }
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
