pipeline{
  agent any
    environment{
      LANG='en_US.UTF-8'
      LC_ALL='en_US.UTF-8'
      }
    tools{
      maven 'Maven'
      }
    stages{
      stage('Checkout'){
        steps{
          git branch:'main', url:'https://github.com/bitcsedevops203/2023Ansible.git'
          }
          }
      stage('Build'){
        steps{
          sh 'mvn clean package'
          }
          }
     
      stage('Deploy'){
        steps{
          sh 'mvn clean package'
          sh 'ansible-playbook playbook.yml -i hosts.ini'
          }
          }
          }
          }
          
