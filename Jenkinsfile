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

    }
}