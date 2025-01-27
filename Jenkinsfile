pipeline {
    agent any

    stages {
        stage('Build & Tag Docker Image') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'animeshnikhare97', toolName: 'docker') {
                        sh "docker build -t rahamshaik/frontend:latest ."
                    }
                }
            }
        }
        
        stage('Push Docker Image') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'animeshnikhare97', toolName: 'docker') {
                        sh "docker push rahamshaik/frontend:latest"
                    }
                }
            }
        }
    }
}
