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
            }
        }
    }
}
