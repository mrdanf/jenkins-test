pipeline {
    agent any

    stages {
        stage ('End - Echo') {
            steps {
                sh 'echo "Hello, END!"'
                sh 'echo "pwd: $(pwd)"'
                sh 'echo "First file yo!" > test.txt'
            }
        }
    }
}
