pipeline {
    agent {
        label 'agent1'
    }
    stages {
        stage('ubuntu_16_04_x86_64') {
            agent {
                dockerfile true { dir 'docker/ubunut_16_04_x86_64' }
            }
            steps {
                sh './configure'
                sh 'make -j8'
            }
        }
    }
}
