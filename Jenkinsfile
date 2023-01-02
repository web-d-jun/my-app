// Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'node:18.5.0' } }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
    }
    post {
        success {
            echo 'successful!'
        }
    }
}
