pipeline {
    agent any
    
    stages {
        stage('triger') {
            when {
                expression {
                    return env.GIT_BRANCH == "dev"
                }
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
                expression {
                    return env.GIT_BRANCH == "master"
                }
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

