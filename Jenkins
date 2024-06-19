pipeline {
    agent any

    stages {
         stage('Docker') {
            agent {
                docker {
                    image 'ubuntu'
                    reuseNode true
                }
            }
            steps {
                echo 'Hello World from docker container'
                sh '''
                cat /etc/os-release > /tmp/output.txt
                cat /tmp/output.txt
                '''
            }
        }
        stage('Hello') {
            steps {
                echo 'Hello World from github'
                sh '''
                cat raw.txt
                '''
            }
        }
    }
}
