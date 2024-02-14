pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        GREETING = 'Hello Jenkins'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                  echo "I wrote shell script"
                  env
                """
            }
        }
    }
    //POST BUILD
    post {
        always {
            echo 'I will always say Hello Again'
        }
         failure {
            echo 'this runs when pipeline is failedused generally to send some alerts'
        }
         success {
            echo 'I will always say Hello when pipeline is susccess'
        }
    }
}