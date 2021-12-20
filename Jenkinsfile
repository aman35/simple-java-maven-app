pipeline {
    agent {
        docker {
            image 'maven:3.8.1-adoptopenjdk-11' 
            args '-u root:sudo -v /var/jenkins_home/.m2:/usr/share/maven/.m2'
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