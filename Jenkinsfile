pipeline {
    agent any
    stages {
        stage ("Install Dependencies"){
            steps {
                sh 'npm install'
            }
        }
        
        stage ("Build"){
            steps {
                sh 'npm run build'
            }
        }
        
        stage('Deploy') {
            when {
                branch 'dev' 
                }
            steps {
                sh 'echo "in dev"'
                }
            
            when {
                branch 'master' 
                }
            steps {
                sh 'echo "in master"'
                }
     

        }
    }
}
