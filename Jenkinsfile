pipeline {
    agent any
    stages {
        stage('Hello') {
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
