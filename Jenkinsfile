pipeline {

   agent any

   stages {

     stage('Install Dependencies') {
        steps {
           sh 'npm install'
        }
     }

     stage('Build to prod') {
        steps {
           sh 'npm run build'
           sh 'echo "sucessfully built the app"'
        }
      }


     stage('Deploy in prod environment') {
        steps {
           sh 'serve -s build'
           sh 'echo "Deployed in staging env..."'
        }
      }

        }

   }

