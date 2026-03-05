pipeline{
    agent any
    stages{
        stage('Git checkout') {
          steps{ 
              git branch: 'main', url: 'https://github.com/Tirupatitata123/jenkins-terraform.git'
        }
        }
        stage('Init') {
          steps{ 
              sh 'terraform init'
        }
        }
        stage('plan') {
          steps{ 
              sh 'terraform plan'
        }
        } 
        stage('validate') {
          steps{ 
              sh 'terraform validate'
        }
        }
        stage('apply') {
          steps{ 
              sh 'terraform apply -auto-approve'
        }
        }
        stage('Success Message') {
            steps {
                echo "Infrastructure has been created successfully"
            }
        }
    }
}
