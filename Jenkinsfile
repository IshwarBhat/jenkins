pipeline {
    agent { any }
    stages {
        stage('build') {
            steps {
                echo 'Building ...'
                sh 'python --version'
            }
        }
        stage('Testing') {
            steps {
                echo 'Testing ...'
            }
        }
    }
}