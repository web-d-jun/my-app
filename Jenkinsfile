// Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
pipeline {
    agent { 
        docker { 
            label 'windows' 
            image 'node:18.5.0' 
        } 
    }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
    }
}
