pipeline {
    agent {
        docker { image 'Pradeepkumar95/php:v1'}
    }
    stages {
        stage('Compile') {
            steps {
                echo 'Compile the source code' 
            }
        }
        stage('Run Unit Tests') {
            steps {
                echo 'Run unit tests from the source code'
                sh 'ls'
                sh 'php -version'
                sh 'composer install'
                sh 'phpunit tests/'
            }
        }
    }
}
