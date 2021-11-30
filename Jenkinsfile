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
                sh 'apt update && apt upgrade'
                sh ' apt install software-properties-common'
                sh ' add-apt-repository ppa:ondrej/php'
                sh ' apt update'
                sh ' apt -y install php7.4'
                sh 'php -version'
            }
        }
    }
}
