pipeline {
    agent any

    stages {
        stage ('End - Echo') {
            steps {
                sh 'echo "Hello, END!"'
                sh 'echo "pwd: $(pwd)"'
                sh 'echo "First file yo!" > test.txt'
                script {
                sh 'cd /home/mrdanf'
                sh 'echo "pwd: $(pwd)"'
                }
            }
        }
    }
}
