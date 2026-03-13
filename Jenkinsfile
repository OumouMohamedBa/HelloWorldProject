pipeline {
    agent any
    stages {
        stage('Compile') {
            steps {
                // On vérifie si le fichier existe et on compile
                sh 'javac HelloWorld.java'
            }
        }
        stage('Run') {
            steps {
                // On exécute la classe compilée
                sh 'java HelloWorld'
            }
        }
    }
    post {
        success {
            echo 'Bravo ! Le programme Java a fonctionné.'
        }
        failure {
            echo 'Erreur de compilation ou d\'exécution.'
        }
    }
}
