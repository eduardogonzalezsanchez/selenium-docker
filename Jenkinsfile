pipeline{

    agent any

    stages{

        stage('Build Jar'){
            steps{
                sh "mvn clean package -DskipTests"
            }
        }

        stage('Build Image'){
            steps {
                sh "docker build -t=edulafragua/selenium ."
            }
        }

        stage('Push image'){
            steps{
                sh "docker push edulafragua/selenium"
            }
        }

    }
}