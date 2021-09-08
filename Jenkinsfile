pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/spamulaparty/hello-world.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t datawire/hello-world .'
            }
        }
        stage('downstream') {
            steps {
                build 'helloworld'
            }
        }
    }
}
