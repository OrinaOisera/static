pipeline {
     agent any
     stages {   
         stage('Upload to AWS') {
              steps {
                  withAWS(region:'us-east-2',credentials:'Jenkins') {
                  sh 'echo "Uploading content with AWS creds"'
                      s3Upload( file:'index.html', bucket:'s3jenkins23', path:'index.html')
                  }
              }
         }
     }
}