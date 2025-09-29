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
                 sh 'mvn clean deploy -Dmaven.test.skip=true'
                }
          }
          stage('Test') {
                steps {
                 echo 'Testing..'
                }
          }
          stage('SonarQube analysis') {
            environment {
                  scannerHome = tool 'muthu-sonar-scanner';
            }
            steps{
                  withSonarQubeEnv('muthu-sonarqube-server') { // If you have configured more than one global server connection, you can specify its name
                  sh "${scannerHome}/bin/sonar-scanner"
                  }
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