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
                sh '/home/mrdanf/bwld/frontend/scripts/test.sh'
            }
        }

}