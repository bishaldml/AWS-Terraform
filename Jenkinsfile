
pipeline {
agent any

stages (List files){
  steps {
    sh 'pwd'
    sh 'ls -ltr'
  }
}
  
stages (Terraform ){
  steps {
    sh 'terraform destroy -auto-approve'
    sh 'terraform init'
    sh 'terraform plan'
    sh 'terraform apply -auto-approve'
    sh 'terraform destroy -auto-approve'
  }
}
  
}
