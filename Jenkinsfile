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
                sh 'curl -Ss https://getcomposer.org/installer | php'
                sh 'mv composer.phar /usr/local/bin/composer'
                sh 'chmod +x /usr/local/bin/composer'
                sh 'composer install' 
                sh 'phpunit tests/'
            }
        }
    }
}
