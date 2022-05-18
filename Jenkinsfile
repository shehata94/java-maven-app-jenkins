#!/usr/bin/env groovy

// library identifier: 'jenkins-shared-library@master', retriever: modernSCM(
//         [$class: 'GitSCMSource',
//          remote: ' https://github.com/shehata94/jenkins-shared-library.git',
//          credentialsId: 'github-credentials'
//         ]
// )


//def gv

pipeline {
    agent any
//     tools {
//         maven 'Maven'
//     }
    stages {
        stage("init") {
            steps {
                script {
//                     gv = load "script.groovy"
                       echo "building the application..."


                }
            }
        }
        stage("build jar") {
            steps {
                script {
//                     buildJar()
                        echo "building the application 2..."
                }
            }
        }
        stage("build and push image") {
            steps {
                script {
                    echo "building the application 2..."
//                     buildImage 'kimohero/demo-app:jma-3.0'
//                     dockerLogin()
//                     dockerPush 'kimohero/demo-app:jma-3.0'
                }
            }
        }
        stage("deploy") {
                environment {
               AWS_ACCESS_KEY_ID = credentials('jenkins_aws_acess_key_id')
               AWS_SECRET_ACCESS_KEY = credentials('jenkins_aws_secret_access_key_id')
            }
            steps {
                script {
         //           gv.deployApp()
                      echo 'deploying docker image...'
                      sh 'kubectl create deployment nginx-deployment --image=nginx'

                }
            }
        }
    }
}
