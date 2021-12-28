pipeline {
    agent any
 tools {
     jdk 'JAVA_HOME' 
        maven "3.8.4" // You need to add a maven with name "3.6.0" in the Global Tools Configuration page
    }
  

    stages {
        stage("get source code") {

             steps  {
                  checkout scm
             }   
        }
        stage("Build") {
            steps {
                sh "mvn -version"
                sh "mvn clean install"
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}