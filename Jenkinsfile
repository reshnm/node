pipeline {
    agent any
    stages {
        stage('Build') {
            parallel {
                agent {
                    label 'master'
                }
                stage('Ubuntu 16.04 x86_64') {
                    agent {
                        dockerfile { dir 'docker/ubuntu_16_04_x86_64' }
                    }
                    steps {
                        sh './configure'
                        sh 'make -j8'
                        sh 'cp out/Release/node node_ubuntu_16_04_x86_64'
                    }
                    post {
                        success {
                            archive 'node_ubuntu_16_04_x86_64'
                        }
                    }
                }
                stage('Fedora 27 x86_64') {
                    agent {
                        dockerfile { dir 'docker/fedora_27_x86_64' }
                    }
                    steps {
                        sh './configure'
                        sh 'make -j8'
                        sh 'cp out/Release/node node_fedora_27_x86_64'
                    }
                    post {
                        success {
                            archive 'node_fedora_27_x86_64'
                        }
                    }
                }
            }
        }
    }
}
