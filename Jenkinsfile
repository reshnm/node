pipeline {
    agent any
    stages {
        agent {
            label 'Linux_x86_64'
        }
        stage('Build') {
            agent {
                dockerfile { dir 'docker/ubuntu_16_04_x86_64' }
            }
            steps {
                sh './configure'
                sh 'make -j8'
            }
        }
    }
}
