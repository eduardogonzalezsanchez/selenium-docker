pipeline{

    agent any

    stages{

        stage('Build Jar'){
            steps{
                bat "mvn clean package -DskipTests"

            }
        }

        stage('Build Image'){
            steps {
                bat "docker build -t=edulafragua/selenium ."
            }
        }

        stage('Push image'){
            steps{
                bat "docker push edulafragua/selenium"
            }
        }

    }
}