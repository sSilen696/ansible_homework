node("linux"){
    stage("Git checkout"){
        git branch: 'main', credentialsId: 'git', url: 'git@github.com:netology-code/mnt-homeworks-ansible.git'
    }
    stage("Sample define secret_check"){
        secret_check=true
    }
    stage("Run playbook"){
        if (secret_check){
            sh 'ansible-playbook playbook/site.yml -i playbook/inventory/prod.yml'
        }
        else{
            echo 'need more action'
        }

    }
}