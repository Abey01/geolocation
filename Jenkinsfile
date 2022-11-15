pipeline {
    agent any
    tools{
        maven 'M2_HOME'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean'
                sh 'mv install'
                sh 'mvn package'
            }
        }
             stage('Test') {
            steps {
                sh 'mvn test'
            }
        }     
         stage('Deploy') {
            steps {
                echo 'Deploy Step'
                sleep 5
            }
        }
         stage('Docker') {
            steps {
                echo 'Image step'
            }
        }    
    }
}