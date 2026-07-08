pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                dir('vehicle-parking') {
                    sh '''
                        mkdir -p build
                        cd build
                        cmake ..
                        make
                    '''
                }
            }
        }
    }
}

