pipeline {
    agent any
    
    stages {
        stage('triger') {
            when {
                branch 'dev' 
            }
            stages {
                stage("install dependencies"){
                    steps {
                        sh 'echo "hii"'
                    }
                }
                stage ("ttt") {
                    steps {
                        sh 'echo "hhhhhh"'
                    }
                }
            }
        }
  
        stage('trigermmmm') {
            when {
                branch 'master' 
            }
            stages {
                stage("install dependencies"){
                    steps {
                        sh 'echo "mmmm"'
                    }
                }
                stage ("ttt") {
                    steps {
                        sh 'echo "kkkkk"'
                    }
                }
            }
        }
    }
}

