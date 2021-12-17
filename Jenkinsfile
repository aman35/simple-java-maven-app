pipeline {
    agent {
        docker {
            image 'maven:3.3.3-jdk-8' 
            args '-v /var/jenkins_home/.m2:/usr/share/maven/.m2 -v /home/git/simple-java-maven-app:/var/jenkins_home/workspace/JPL'
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