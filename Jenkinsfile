pipeline {
    agent any

    stages{
        stage('Build Docker Image') {
            steps {
                script {
                    dockerapp = docker.build("gabriellcruz/python-test:${env.BUILD_NUMBER}", '-f /.src/Dockerfile', './src')
                }
            }
        }

        stage('Push Docker Image') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
                        dockerapp.push('latest')
                        dockerapp.push("${env.BUILD_NUMBER}")
                    }
                }
            }
        }
        // stage('Deploy no Kubernetes') {
        //     steps {
                
        //     }
        // }
    }
}