pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/prashanth3516/jenkin-terraform-job.git'
            }
        }

        stage('terraform Init') {
            steps {
                sh 'terraform init'
            }
        }

        stage('terraform Validate') {
            steps {
                sh 'terraform validate'
            }
        }

        stage('terraform Plan') {
            steps {
                sh 'terraform plan -out=tfplan'
            }
        }

        stage('terraform Apply') {
            steps {
                sh 'terraform apply -auto-approve tfplan'
            }
        }
    }
}
