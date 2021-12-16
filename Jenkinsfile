pipeline {
    agent {
        docker {
            image 'maven:3.3.3-jdk-8' 
            args '-v /mnt/c/Users/Amandeep_Sharma/Downloads/m2:/var/maven/.m2 -e MAVEN_CONFIG=/var/maven/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}