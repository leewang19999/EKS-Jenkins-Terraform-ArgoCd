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

    
    stage('Terraform init') {
      steps {
        dir('Terraform') {
            sh 'terraform init '
            sh 'terraform plan '
          }
      }
    }
        
  }
}
