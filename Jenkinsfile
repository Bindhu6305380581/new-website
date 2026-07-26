pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/Bindhu6305380581/new-website.git'
            }
        }

        stage('Verify Files') {
            steps {
                sh 'ls -la'
            }
        }

        stage('Archive Website') {
            steps {
                archiveArtifacts artifacts: '**/*', fingerprint: true
            }
        }

    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
