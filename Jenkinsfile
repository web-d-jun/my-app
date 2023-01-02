// Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'node:18.5.0' } }
    environment {
        URL_WEBHOOK = 'https://goodksoft.webhook.office.com/webhookb2/e43d25f3-4330-4d83-9796-1881f9212718@a1496fa5-ec0f-4cad-95ea-80a285b77c8a/IncomingWebhook/96b08c173e1c423b9726f12dc79a4dc2/e9476b45-b5f5-4f86-a3fb-a6172611bd8f'
    }
     options {
        office365ConnectorWebhooks([
            [name: "Office 365", url: "${URL_WEBHOOK}", notifyBackToNormal: true, notifyFailure: true, notifyRepeatedFailure: true, notifySuccess: true, notifyAborted: true]
        ])
    }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
    }
    post {
        success {
            echo 'successful! '${URL_WEBHOOK}''
        }
    }
}
