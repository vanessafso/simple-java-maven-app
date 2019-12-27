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

        stage("Analise:Sonar")
            steps {
                sh '$MVN sonar:sonar \
                -Dsonar.projectKey=BecaDevOps:master \
                -Dsonar.host.url=http://localhost:9000 \
                -Dsonar.login=27ca10209b96d30b390a090ee085564f0e923778'
            }
        }


    }
}