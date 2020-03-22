pipeline {
    agent any

    stages {
        stage('initialize') {
            steps {
                sh 'whoami'
                sh 'node --version'
                sh 'npm -version'
            }
        }
        stage('npm-install') {
            steps {
                echo "Branch is ${env.BRANCH_NAME}..."
                sh 'npm install'
            }
        }
    }
}
