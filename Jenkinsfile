pipeline {
    agent {
        docker { image 'node:14-alpine' }
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
                sh 'phpunit tests/'
            }
        }
    }
}
