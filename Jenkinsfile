pipeline {
    agent {
        label 'linux'
    }
    stages {
        stage('Checkout') {
            steps{
                git credentialsId: 'git', url: 'git@github.com:sSilen696/ansible_homework.git'
            }
        }
        stage('Install molecule') {
            steps{
                sh 'pip3 install -r test-requirements.txt'
                sh "echo =============="
            }
        }
        stage('Run Molecule'){
            steps{
                sh 'molecule test'
            }
        }
    }
}