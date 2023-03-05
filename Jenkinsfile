pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'dev') {
                        stages{
                            stage('test'){
                                steps {
                                    echo "hhhh"
                                }
                            }
                        }
                    }  else {
                        sh "echo 'Hello from ${env.BRANCH_NAME} branch!'"
                    }
                }
               
            }
        }
    }
}
