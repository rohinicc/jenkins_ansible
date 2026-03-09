pipeline{
    agent any
    environment{
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }
    stages{
        stage('pull for git repo'){
            steps{
                git branch = 'main',url:'https://github.com/rohinicc/jenkins_ansible.git'
           }
        }
            steps{
                sh """
                su - ansible -c "ansible-playbook -i 172.31.5.196 playbook.yml"               
                """
            }
        }
    }

