pipeline {
    agent any

    stages {
        stage('Build & Tag Docker Image') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'animeshnikhare97', toolName: 'docker') {
                        sh "docker build -t animeshnikhare97/checkoutservice:latest ."
                    }
                }
            }
        }
        
        stage('Push Docker Image') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'animeshnikhare97', toolName: 'docker') {
                        sh "docker push animeshnikhare97/checkoutservice:latest "
                    }
                }
            }
        }
    }
}
