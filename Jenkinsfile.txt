pipeline {
    agent any 

    stages {
        stage('complie') { 
            steps { 
                sh 'mvn compile' 
            }
        }
        stage('Test'){
            steps {
                sh 'mvn test' 
            }
        }
        stage('Deploy') {
            steps {
                sh 'make deploy'
            }
        }
    }
}