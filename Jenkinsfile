pipeline {
    agent {
       label 'agent'
           }
     tools {
      maven 'maven339'
          }        
    stages {
        stage('Build') { 
            steps {
               sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
