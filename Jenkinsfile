pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Récupère le code depuis GitHub
                checkout scm
            }
        }
        stage('Compile') {
            steps {
                script {
                    // Compile le fichier Java
                    sh 'javac HelloWorld.java'
                }
            }
        }
        stage('Run') {
            steps {
                script {
                    // Exécute le programme
                    sh 'java HelloWorld'
                }
            }
        }
    }
    
    post {
        success {
            echo '✅ Succès : Le code a été compilé et exécuté !'
        }
        failure {
            echo '❌ Erreur : Quelque chose a échoué.'
        }
    }
}
