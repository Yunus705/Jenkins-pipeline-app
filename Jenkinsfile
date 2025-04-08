pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the app...'
                sh 'docker build -t myapp .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "No tests to run."'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the app...'
                sh 'docker run -d -p 9000:3000 myapp'
            }
        }
    }
}
