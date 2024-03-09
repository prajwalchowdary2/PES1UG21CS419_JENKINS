pipeline {
    agent any
    stages {
            stage('Build') {
            steps {
                build 'pes1ug21cs419-1'
                sh 'g++ cccc.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
