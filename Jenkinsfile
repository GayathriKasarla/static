pipeline {
    agent any
    stages {
       stage('Hello and Upload to AWS') {
             steps {
                 sh 'echo "Hello World"' 
                 withAWS(region: 'us-east-1', credentials: 'awsstatic') {
                 sh 'echo "Uploading content with AWS creds"'
                     //s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'udagram-pipeline')
                    sh 'echo "Hello World"' 
                 }
             }
        }
    }
}
