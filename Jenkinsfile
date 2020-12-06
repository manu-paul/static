pipeline {
     agent any
     stages {
         stage('Upload to AWS') {
              steps {
                  withAWS(region:'us-east-2',credentials:'aws-static') {
                  sh 'echo "Uploading content to S3 with AWS credentials"'
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkins-prj3')
                  }
              }
         }
     }
}
