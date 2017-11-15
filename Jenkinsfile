pipeline {
    agent {
        label 'Linux_x86_64'
    }
    stages {
        stage('ubuntu_16_04_x86_64') {
            agent {
                dockerfile { dir 'docker/ubunut_16_04_x86_64' }
            }
            steps {
                sh './configure'
                sh 'make -j8'
            }
        }
    }
}
