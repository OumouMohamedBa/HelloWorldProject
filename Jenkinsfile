pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                // Pas besoin de stage "Checkout", Jenkins le fait déjà seul
                sh 'javac HelloWorld.java'
            }
        }
        stage('Run') {
            steps {
                sh 'java HelloWorld'
            }
        }
    }
    
    post {
        success {
            echo ' Succès !'
        }
        failure {
            echo ' Échec.'
        }
    }
}
