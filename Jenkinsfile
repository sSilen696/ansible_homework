node("linux"){
    stage("Git checkout"){
        git branch: 'main', credentialsId: 'git', url: 'git@github.com:sSilen696/ansible_homework.git'
    }

    stage("Run playbook"){
        if (params.run_prod){
            sh 'cd playbook/ && ansible-playbook site.yml -i inventory/prod/hosts.yml -check --diff'
        }
        else{
            sh 'cd playbook/ && ansible-playbook site.yml -i inventory/prod/hosts.yml'
        }

    }
}