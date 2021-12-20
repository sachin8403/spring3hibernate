pipeline{
    agent any
    stages{
        stage('Clone Code') {
            steps {
                git changelog: false, credentialsId: 'sachin-git-cred', poll: false, url: 'https://github.com/sachin8403/spring3hibernate.git'
            }
        }
        stage("Compilation"){
            steps{
                sh 'mvn clean package'
            }
        }
        stage("Test"){
            steps{
                sh 'mvn test'
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
