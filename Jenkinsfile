pipeline{
    agent any
    stages{
        stage('Clone Code') {
            steps {
                git changelog: false, credentialsId: 'sachin-git-cred', poll: false, url: 'https://github.com/sachin8403/spring3hibernate.git'
            }
        }
        stage("validate"){
            steps{
                sh 'mvn validate'
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
