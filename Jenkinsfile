node("linux"){
    stage("Git checkout"){
        git branch: 'main', credentialsId: 'git', url: 'git@github.com:sSilen696/ansible_homework.git'
    }

    stage("Run playbook"){
        dir('playbook') {
            if (params.run_prod){
                sh 'ansible-playbook site.yml -i inventory/prod/hosts.yml -check --diff'
            }
            else{
                sh 'ansible-playbook site.yml -i inventory/prod/hosts.yml'
            }
        }
    }
}