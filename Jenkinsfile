pipeline {
    agent any

    stages{
        stage('Build Docker Image') {
            steps {
                script {
                    // dockerapp = docker.build("gabriellcruz/python-test:${env.BUILD_ID}", '-f /.src/Dockerfile', './src')
                    sh 'docker build -f src/Dockerfile .'
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