pipeline {
    agent {
       label 'agent'
           }
     tools {
      maven 'maven354'
          }        
    stages {
        stage('Build') { 
            steps {
               sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
