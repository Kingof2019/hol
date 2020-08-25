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
        
        stage('test') {
            steps {
                sh 'mvn test'
                    
            }
        }    
         stage('created and push docker image') {
            steps {
                script {
                  checkout scm
                    docker.withRegistry( '', 'DockerRegistryId' ) {
                        def customImage = docker.bluid("sani1/holi-pipeline:${env.BLUID_ID}")
                        customImage.push()
                    }
                }
            }
         }  
      }
}

