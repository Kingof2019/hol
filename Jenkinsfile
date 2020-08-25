pipeline {
    
    agent any
    tools {
        maven 'M2_HOME'
    }
    stages {
        stage('bluid') {
            steps {
                echo 'Hello World'
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
                
            }
        }
        
        stage('deploy') {
            steps {
                echo 'Hello deploy'
            }
        }
       
       
         stage('test') {
            steps {
                echo 'Hello test'
            }
        
         }
        
        stage('test') {
            steps {
                echo 'Hello test'
            }
        }
    }
    
}  
        

