pipeline {
  agent any

  environment {
    AWS_ACCESS_KEY_ID = 'AKIA33V37KOHG45DCAX6'
    AWS_SECRET_ACCESS_KEY = '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'
    AWS_DEFAULT_REGION = 'us-east-1'
  }

  stages {
    stage('git') {
        steps {
            sh 'git init'
            sh "https://github.com/Chaarvi7550/terra12"
        }
    }
    stage('Terraform Init') {
      steps {
        sh 'terraform init'
      }
    }

    stage('Terraform Plan') {
      steps {
        sh 'terraform plan -out=tfplan'
      }
    }

    stage('Terraform Apply') {
      steps {
        sh 'terraform apply tfplan'
      }
    }
  }
}
