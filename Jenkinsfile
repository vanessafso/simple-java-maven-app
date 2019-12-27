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
                sh '$MVN -B -DskipTests clean package' 
            }
        }

        stage("Analise:Sonar") {
            steps {
                sh '$MVN sonar:sonar \
                -Dsonar.projectKey=beca-devops:master \
                -Dsonar.host.url=http://104.198.195.37:9000 \
                -Dsonar.login=3c96f435cc4ae56591ace5a56ed078cea3fe156a'
            }
        }


    }
}