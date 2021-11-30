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
                sh 'apt install -y wget php-cli php-zip unzip'
                sh 'php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"'
                sh 'HASH="$(wget -q -O - https://composer.github.io/installer.sig)"'
                sh 'php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"'
                sh 'php composer-setup.php --install-dir=/usr/local/bin --filename=composer'
                sh 'composer' 
                sh 'phpunit tests/'
            }
        }
    }
}
