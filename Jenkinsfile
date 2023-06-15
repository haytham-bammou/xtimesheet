pipeline {
    agent any
    
    stages {
        stage('Build Project') {
            steps {
                input(message: 'Choose environment:', parameters: [
                    choice(choices: 'dev\nqa\nprod', description: 'Select environment', name: 'ENVIRONMENT')
                ])
                script {
                    def environment = env.ENVIRONMENT
                    echo "Selected environment: ${environment}"
                    sh "sleep 40s"
                }
            }
        }
        
        stage('Build image') {
            steps {
                echo 'Pushing image...'
                sh "sleep 50s"
            }
        }

        stage('Push image') {
            steps {
                echo 'Pushing image...'
                sh "sleep 100s"
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh "sleep 120s"
            }
        }
    }
}