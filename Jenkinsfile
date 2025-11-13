pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/kolaganiReeha/portfolio'
            }
        }

        stage('Build') {
            steps {
                echo "No build needed for static HTML project"
            }
        }

        stage('Archive Artifact') {
            steps {
                archiveArtifacts artifacts: '**/*', fingerprint: true
            }
        }
    }

    post {
        success {
            echo "Pipeline succeeded!"
        }
        failure {
            echo "Pipeline failed!"
        }
    }
}
