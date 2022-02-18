pipeline {
    agent none
    stages {
        stage('Run builds') {
            parallel {
                stage('Node install') { 
                    agent { label 'u20-nodejs16-yarn' }
                    steps {
                        sh 'cd node && npm install' 
                        }
                }
                stage ('Maven Install') {
                    agent { label 'u20-mvn-jdk8' }
                    steps {
                        sh 'cd maven && mvn clean install' 
                    }
                }
                }
        }

        
    }
}

