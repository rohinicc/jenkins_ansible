pipeline{
    agent any
    environment{
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }
    stages{
        stage('pull for git repo'){
            steps{
                git branch : 'main' , url:'https://github.com/rohinicc/jenkins_ansible.git'
           }
        }
        stage('run ansible playbook'){
            steps{
                sh """
                ansible-playbook -i inventory playbook.yml               
                """
            }
        }
        
        }
    }

