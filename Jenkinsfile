pipeline {
    agent none
    stages {
        stage('Node install') { 
            agent { label 'u20-nodejs16-yarn' }
            steps {
                sh 'npm install' 
            }
        }
        stage ('Maven Install') {
            agent { label 'u20-mvn-jdk8' }
            steps {
                sh 'mvn clean install' 
            }
        }
    }
}
