pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    //Variável de construção da imagem Docker
                    sh pwd
                }
            }
        }

        stage('Push Docker Image') {
            steps {
                script {
                    //Criando a conexão com o Docker Hub para power enviar a imagem criada no Step anterior
                    sh '"Aqui vai os comandos do step 2"'
                }
            }
        }
        
        stage('Deploy no Kubernetes') {
            steps {
                sh '"Aqui vai os comandos do step 3"'
            }
        }
    }
}
