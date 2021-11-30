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
                sh 'apt clean & apt-get -y update && apt-get -y upgrade'
                sh ' apt -y install php7.4'
                sh 'php -version'
                sh 'ls'
                sh 'composer update' 
                sh 'phpunit tests/'
            }
        }
    }
}
