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
        }
        stage('Deploy-image') {
            steps{
                echo "Deploying image"
                sh 'docker compose up'
            }
        }
    }
}