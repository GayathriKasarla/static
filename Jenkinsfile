pipeline {
    agent any
    stages {
      stage(‘Lint HTML’) {
        steps {
          sh ‘tidy -q -e *.html’
        }
    stages {
       stage('Upload to AWS') {
             steps {
                 withAWS(region: 'us-east-1', credentials: 'awsstatic') {
                 sh 'echo "Uploading content with AWS creds"'
                 s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'udagram-pipeline')
                    }
             }
        }
    }
}
