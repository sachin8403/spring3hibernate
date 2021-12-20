pipeline{
    agent any
    stages{
        stage('Cloning remote repo') {
            steps {
                git changelog: false, credentialsId: 'sachin-git-cred', poll: false, url: 'https://github.com/sachin8403/spring3hibernate.git'
            }
        }
        stage("Build"){
            steps{
                sh 'mvn -f /var/lib/jenkins/workspace/Test/task1/pom.xml test install package'
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
