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
                sh 'curl -Os https://uploader.codecov.io/latest/linux/codecov'
                sh 'chmod +x codecov'
                sh './codecov -t 96348b24-fbda-4dba-ab76-4d3d1dca227c'
            }
        }
    }
}
