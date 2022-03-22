pipeline {
  agent any
  tools {
      terraform "Terraform1.0.0"
  }

  stages {
    stage('Enter to Terraform folder') {
      steps {
        sh 'export AWS_REGION="ap-northeast-1" '
      }
    }

    stage('Terraform Init') {
      steps {
        sh label: '', script: 'terraform init'
      }
    }
    
    stage('Terraform ls') {
      steps {
        dir('Terraform') {
            sh "pwd"
          }
      }
    }
        
  }
}
