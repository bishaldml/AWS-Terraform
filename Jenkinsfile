
pipeline {
agent any

stages {
  steps ("List files") {
    sh 'pwd'
    sh 'ls -ltr'
  }
}
  
stages {
  steps ("Terraform") {
    sh 'terraform destroy -auto-approve'
    sh 'terraform init'
    sh 'terraform plan'
    sh 'terraform apply -auto-approve'
    sh 'terraform destroy -auto-approve'
  }
}
  
}
