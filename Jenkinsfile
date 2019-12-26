pipeline {
    agent any
   
    stages{


        stage ('checkout:git') {
            git branch: "master", url: "https://github.com/vanessafso/simple-java-maven-app.git"
        }

        stage('Build:Maven') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }

    }
}