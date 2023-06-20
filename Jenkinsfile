
pipeline {
agent any
stages{
  
  stage ("List files") {
  steps {
    sh 'pwd'
    sh 'ls -ltr'
  }
}
  
  stage ("Terraform") {
    steps {
      sh 'terraform destroy -auto-approve'
      sh 'terraform init'
      sh 'terraform plan'
      sh 'terraform apply -auto-approve'
      sh 'terraform destroy -auto-approve'
  }
} 
  
}
}
  

