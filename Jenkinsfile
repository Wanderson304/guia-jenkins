//Exemplo de um arquivo jenkisfile
//A extenção do arquivo não é .js coloquei apenas para ter uma formatação minima.

pipeline {
    agent any

    stages {
        stage('Titulo Step 1') {
            steps {
                //Screva o estep aqui
                sh 'echo "Executando o comando Docker Build"'
            }
        }
        
        stage('Titulo Step 2') {
            steps {
                //Screva o estep aqui
                sh 'echo "Executando o comando Docker push"'
            }
        }
        
        stage('Titulo Step 3') {
            steps {
                //Screva o estep aqui
                sh 'echo "Executando o comando Docker kubectl apply"'
            }
        }
    }
}
