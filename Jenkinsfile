pipeline {
    agent any
    
    stage('push triger') {
            when {
                branch 'dev' 
            }
            steps {
                script {
                    properties([pipelineTriggers([githubPush()])])
                }
                //define scm connection for polling
                git branch: dev, credentialsId: ' ', url: 'https://github.com/girishbm4567/nodejs-demo.git'
                checkout scm: [$class: 'GitSCM',
                    userRemoteConfigs: [[url: 'https://github.com/girishbm4567/nodejs-demo.git',
                                        credentialsId: ' ']],
                                         branches: [[name: 'origin/master']]
                ]
            }
        }
    stage('poll scm') {
            when {
                branch 'master'  
            }
            steps {
                script {
                    properties([pipelineTriggers([pollSCM('')])])
                }
                //define scm connection for polling
                git branch: master, credentialsId: '', url: 'https://github.com/girishbm4567/nodejs-demo.git'
                checkout scm: [$class: 'GitSCM',
                    userRemoteConfigs: [[url: 'https://github.com/girishbm4567/nodejs-demo.git',
                                        credentialsId: ' ']],
                                         branches: [[name: 'origin/master']]
                ]
            }
        }
    
    
    
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
        stage('Deliver for development') {
            when {
                branch 'dev' 
            }
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
        stage('Deploy for production') {
            when {
                branch 'master'  
            }
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
}
