pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'cd webapp && npm install'
                sh 'cd webapp && npm run build'
                echo 'modified'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'scp -r webapp/dist ubuntu@3.101.47.190:/home/ubuntu/dist'
                
            }
        }
    }
}
