pipeline {
  agent any

  environment {
    AWS_ACCESS_KEY_ID = 'AKIAVZG7PMN4OLAE6D4W'
    AWS_SECRET_ACCESS_KEY = '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'
    AWS_DEFAULT_REGION = 'us-east-1'
  }

  stages {
    stage('git') {
        steps {
            sh 'git init'
            sh "git pull https://github.com/usharanigudala707/terra.git"
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
