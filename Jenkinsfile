pipeline {
    agent any

    stages{
        stage('Build Docker Image') {
            steps {
                script {
                    dockerapp = docker.build("gabriellcruz/python-test:${env.BUILD.ID}", '-f /.src/Dockerfile', './src')
                }
            }
        }
        // stage('Push Docker Image') {
        //     steps {
                
        //     }
        // }
        // stage('Deploy no Kubernetes') {
        //     steps {
                
        //     }
        // }
    }
}