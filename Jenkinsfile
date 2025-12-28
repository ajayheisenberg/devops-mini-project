pipeline {
    agent any

    stages {
        stage('Pull Code') {
            steps {
                git branch: 'master', url: 'https://github.com/ajayheisenberg/devops-mini-project'
            }
        }

        stage('Build') {
            steps {
                echo "Building project..."
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                     mkdir -p /home/ajay/devops-project/
                     cp -r * /home/ajay/devops-project/
                '''
            }
        }
    }

    post {
        success {
            echo "Deployment successful!"
        }
        failure {
            echo "Something went wrong!"
        }
    }
}
