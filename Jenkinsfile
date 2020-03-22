pipeline {
    agent {
        docker {
            image 'node:latest'
            args '-p 3000:3000 -p 5000:5000'
            args '-u 0:0'
        }
    }

    stages {
        stage('initialize') {
            steps {
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
