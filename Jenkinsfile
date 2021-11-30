pipeline {
    agent {
        docker { image 'php:7.3' }
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
                sh 'php -version'
                sh 'composer'
                sh 'phpunit tests/'
            }
        }
    }
}
