pipeline {
    agent any

    stages {
        stage('download repo') {
            steps {
                git credentialsId: 'git', url: 'git@github.com:sSilen696/ansible_homework.git'
            }
        }
        stage('install requirements') {
            steps {
                sh 'pip install -r test-requirements.txt'
            }
        }
        stage('molecule test') {
            steps {
                sh 'molecule test'

            }
            }
    }
}