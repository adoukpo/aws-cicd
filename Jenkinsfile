pipeline {
    agent any

    environment {
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/adoukpo/aws-cicd.git'
        IMAGE_TAG = 'adoukpo/aws-cicd'
        IMAGE_VERSION = "${BUILD_NUMBER}"
    }
    stages {
    stage('git checkout'){
        steps{
        git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
        }
    }
    stage('ls'){
        steps{
            sh 'echo ls'
        }
    }
    stage('test'){
        steps{
            sh 'echo test'
        }
    }
    stage('pwd'){
        steps{
            sh 'echo pwd'
        }
    }
    stage('nproc'){
        steps{
            sh 'echo nproc'
        }
    }
    stage('whoami'){
        steps{
            sh 'echo whoami'
        }
    }
    stage('docker build'){
        steps{
            sh 'docker build -t "${IMAGE_TAG}:${IMAGE_VERSION}" .'
            sh 'docker images'
        }
    }
    }
}