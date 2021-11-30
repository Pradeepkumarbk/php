pipeline {
    agent {
        docker { image 'pradeepkumar95/php:v3'}
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
                sh 'composer update'
                sh 'phpunit tests/'
                sh 'vendor/bin/phpunit --coverage-clover coverage.xml'
                sh 'bash <(curl -s https://codecov.io/bash) -t 96348b24-fbda-4dba-ab76-4d3d1dca227c'
            }
        }
    }
}
