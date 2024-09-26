pipeline {
    agent any

    environment {
      BRANCH_NAME ='MAIN'
      GIT_URL = 'https://github.com/dammy0404/aws-cicd.git'
    }
    
    stages {
      stage('git checkout'){
        steps{
          git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
        }
      }
      stage('docker build'){
        steps{
          sh 'docker build -t aws-cicd .'
          sh 'docker images'
        }
      }
    }
}