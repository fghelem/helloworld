pipeline {
    agent any
 tools {
    java 'JAVA_HOME' 
        maven 'MAVEN_HOME'
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