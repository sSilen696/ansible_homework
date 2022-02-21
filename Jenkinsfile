node("linux"){
    stage("Git checkout"){
        git branch: 'main', credentialsId: 'git', url: 'git@github.com:sSilen696/ansible_homework.git'
    }
    stage("Sample define secret_check"){
        secret_check=false
    }
    stage("Run playbook"){
        if (secret_check){
            sh 'ansible-playbook playbook/site.yml -i playbook/inventory/prod/hosts.yml -check --diff'
        }
        else{
            sh 'ansible-playbook playbook/site.yml -i playbook/inventory/prod/hosts.yml'
        }

    }
}