pipeline {
    agent {
        node{
            label 'MB_agent'
        }
    }
    stages {
        stage('---clean---') {
            steps {
                sh "mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package"
            }
        }
        triggers {
    pollSCM('*****') // Enabling being build on Push
  }
    }
}
