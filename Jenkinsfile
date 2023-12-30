pipeline{
    agent any
    stages{
        stage('Build-image') {
            steps{
                sh'''
                docker build -t nikeshhh/phpapp-intuji .
                docker push nikeshhh/phpapp-intuji
                '''
            }
            post{
                success{
                    echo "Archiving the Dockerfile....."
                    archiveArtifacts artifacts: 'Dockerfile'
                }
            }
        }
        stage('Deploy-image') {
            steps{
                echo "Deploying image"
                sh 'docker compose up'
            }
        }
    }
}