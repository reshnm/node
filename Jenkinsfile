pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './configure'
                sh 'make -j8'
            }
        }
    }
}
