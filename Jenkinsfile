//Exemplo de um arquivo jenkisfile
//A extenção do arquivo não é .js coloquei apenas para ter uma formatação minima.

pipeline {
    agent any

    stages {
        stage('Step 1') {
            steps {
                //Screva o estep aqui
                sh 'echo "Executando o comando Docker Build"'
            }
        }
        
        stage('Step 2') {
            steps {
                //Screva o estep aqui
                sh 'echo "Executando o comando Docker push"'
            }
        }
        
        stage('Step 3') {
            steps {
                //Screva o estep aqui
                sh 'echo "Executando o comando Docker kubectl apply"'
            }
        }
    }
}