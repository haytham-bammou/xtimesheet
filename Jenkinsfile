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
                }
            }
        }
        
        stage('Build image') {
            steps {
                echo 'Pushing image...'
            }
        }

        stage('Push image') {
            steps {
                echo 'Pushing image...'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}