pipeline{
    agent any
    stages{
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
