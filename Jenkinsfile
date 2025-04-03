pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    //Variável de construção da imagem Docker
                    dockerapp = docker.build("Wanderson304/guia-jenkins:${env.BUILD_ID}", '-f ./src/Dockerfile ./src')
                }
            }
        }

        stage('Push Docker Image') {
            steps {
                script {
                    //Criando a conexão com o Docker Hub para power enviar a imagem criada no Step anterior
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
                    //Enviar a imagem dockerapp para o Docker Hub.
                    dockerapp.push('latest')
                    dockerapp.push("${env.BUILD_ID}")
                    }
                }
            }
        }
        
        stage('Deploy no Kubernetes') {
            steps {
                sh 'echo "Executando o comando Docker kubectl apply"'
            }
        }
    }
}
