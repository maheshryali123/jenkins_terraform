pipeline {
    agent { label 'SPRING' }
    stages {
        stage('git_clone') {
            steps {
                git branch: 'main',
                       url: 'https://github.com/maheshryali123/jenkins_terraform.git'
            }
        }
        stage('ansible') {
            steps{
                 sh """
                 terraform init
                 terraform apply -auto-approve
                 """
            }
        }
    }
}