//Exemplo de um arquivo jenkisfile
//A extenção do arquivo não é .js coloquei apenas para ter uma formatação minima.
//Aqui usamos os Plugins do Docker e Kubernetes instalado no Jenkins

pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    //Variável de construção da imagem Docker
                    //dockerapp = docker.build("Wanderson304/guia-pratico-jenkins:${env.BUILD_ID}", '-f ./src/Dockerfile ./src')
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

