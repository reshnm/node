pipeline {
    agent any
    stages {
        stage('Ubuntu 16.04 x86_64') {
            agent {
                dockerfile { dir 'docker/ubuntu_16_04_x86_64' }
            }
            steps {
                sh './configure'
                sh 'make -j8 clean all'
            }
        }
        stage('Fedora 27 x86_64') {
            agent {
                dockerfile { dir 'docker/fedora_27_x86_64' }
            }
            steps {
                sh './configure'
                sh 'make -j8 clean all'
            }
        }
    }
}
