pipeline {
    agent ubuntu_16_04_x86_64

    stages {
        stage('Build') {
            steps {
                sh './configure'
                sh 'make -j8'
            }
        }
    }
}
