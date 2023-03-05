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
            steps {
                script {
                    if (env.BRANCH_NAME == 'dev') {
                        echo "ddddd"
                    }  else {
                        sh "echo 'Hello from ${env.BRANCH_NAME} branch!'"
                    }
                }
               
            }
        }
    }
}
