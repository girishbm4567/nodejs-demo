pipeline {
    agent any
    
    stages {
        stage('triger') {
            steps {
                script {
                    if (env.BRANCH_NAME != 'master') {
                        stages {
                             stage("install dependencies"){
                                 steps {
                                     sh 'echo "hii"'
                                 }
                             }
                            stage("hhhhhhh"){
                                 steps {
                                     sh 'echo "hihhhhhi"'
                                 }
                             }
                        }
                    } else {
                        stages {
                             stage("install dependencies"){
                                 steps {
                                     sh 'echo "hiddddddddi"'
                                 }
                             }
                            stage("hhhhhhh"){
                                 steps {
                                     sh 'echo "hihhhddddddhhi"'
                                 }
                             }
                        }
                    }  
                    
                }
            }
        }
    }
}
           

