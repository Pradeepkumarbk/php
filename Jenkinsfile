pipeline {
    agent any 
    stages {
        stage('Compile') {
            steps {
                echo 'Compile the source code' 
            }
        }
        stage('Run Unit Tests') {
            steps {
                echo 'Run unit tests from the source code' 
                sh 'cat /etc/os-release '
                sh 'apt-get update && apt-get upgrade'
                sh ' apt -y install php7.4'
                sh 'php -version'
            }
        }
    }
}
