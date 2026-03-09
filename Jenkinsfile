pipeline{
    agent any
    environment{
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }
    stages{
        stage('pull for git repo'){
            steps{
                git_branch = 'main'

                url:'https://github.com/rohinicc/ansible_jenkins'
           }
         steps{
                sh """
                su - ansible -c "ansible-playbook -i 172.31.5.196 playbook.yml"               
                """
            }
        }
    }
}
