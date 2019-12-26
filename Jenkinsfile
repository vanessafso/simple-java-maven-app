pipeline {
    agent any
   
    stages{


        stage ('checkout:git') {
            steps{
                echo "Checkout git"
            }
        }

        stage('Build:Maven') { 
            steps {
                sh '/var/jenkins_home/tools/hudson.tasks.Maven_MavenInstallation/MAVEN/bin/mvn -B -DskipTests clean package' 
            }
        }

    }
}