pipeline { 
  
   agent any

   stages {
   
     stage('Install Dependencies') { 
        steps { 
           sh 'npm install' 
        }
     }
     
     stage('Deploy in Dev Env') { 
        steps { 
           sh 'npm start'
           sh 'echo "Deployed in Dev env"'
        }
      }

      

   }
}
