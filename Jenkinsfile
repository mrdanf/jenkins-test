pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                sh '/home/mrdanf/bwld/scripts/pull.sh'
            }
        }

        stage('Frontend Build and Copy') {
            steps {
                sh '/home/mrdanf/bwld/scripts/publishFrontend.sh'
            }
        }

        stage('Backend Build and Copy') {
            steps {
                sh '/home/mrdanf/bwld/scripts/publishBackend.sh'
            }
        }

        stage('Restart') {
            steps {
                sh '/home/mrdanf/bwld/scripts/restart.sh'
            }
        }
    }
}