pipeline {
    agent {
        docker { image 'pradeepkumar95/php:v1'}
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
                sh 'phpunit --version'
                sh 'composer update'
                sh 'phpunit tests/'
            }
        }
    }
}
