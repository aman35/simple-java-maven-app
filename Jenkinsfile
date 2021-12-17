pipeline {
    agent {
        docker {
            image 'maven:3.3.3-jdk-8' 
            args '-v /var/jenkins_home/.m2:/usr/share/maven/.m2 -v /home/git/simple-java-maven-app:/home/git/simple-java-maven-app'
            customWorkspace '/home/git/simple-java-maven-app'
        }
    }
    stages {
        stage('Build') { 
            steps {
               sh 'mvn -B -DskipTests clean package -Dorg.jenkinsci.plugins.durabletask.BourneShellScript.LAUNCH_DIAGNOSTICS=true' 
            }
        }
    }
}