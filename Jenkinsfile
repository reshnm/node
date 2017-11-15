pipeline {
    agent any
    stages {
        stage('Build') {
            node('Linux_x86_64') {
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
}
