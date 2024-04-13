pipeline {
    agent any

    stages {
        stage ('Start - Echo') {
            steps {
                sh 'echo "Hello, START!"'
            }
        }

        stage('Prepare') {
            steps {
                sh 'git -C /home/mrdanf/bwld/frontend pull'
                sh 'git -C /home/mrdanf/bwld/backend pull'
            }
        }

        stage('Frontend Build and Copy') {
            steps {
                sh '/home/mrdanf/bwld/frontend/scripts/publishFrontend.sh'
            }
        }

        stage('Backend Build and Copy') {
            steps {
                sh '/home/mrdanf/bwld/frontend/scripts/publishBackend.sh'
            }
        }

        stage('Restart') {
            steps {
                sh '/home/mrdanf/bwld/frontend/scripts/restart.sh'
            }
        }

        stage ('End - Echo') {
            steps {
                sh 'echo "Hello, END!"'
            }
        }
    }
}