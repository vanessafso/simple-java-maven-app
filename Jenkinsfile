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
                -Dsonar.login=c3372cee3092ec47b72b7a5359b39fbb9c34054c'
            }
        }


    }
}