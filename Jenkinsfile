pipeline {
/*           */
    agent any
    stages {
        stage('docker build') {
            steps {
                sh "docker build -t pruebacicd ."
                sh "docker tag pruebacicd ineslie/nodecicd:${BUILD_NUMBER}"
            }
        }
        stage('docker push') {
            steps {
                /* sh "echo $dockerhub_PSW | docker login -u $dockerhub_USR --password-stdin" */
                sh "docker push ineslie/nodecicd:${BUILD_NUMBER}"
            }
        }
    }
}
