pipeline {
    agent any
    environment {
        // Ajoute le chemin de kubectl au PATH pour qu'il soit accessible partout dans le pipeline
        PATH = "/usr/local/bin:$PATH"
    }
    stages {
        stage('Build') {
            steps {
                // Construit l'image Docker en utilisant le Dockerfile situé à la racine du répertoire de travail.
                sh 'docker build -t mon_app_flask .'
            }
        }
        
        stage('Deploy') {
            steps {
                // Applique le fichier deployment.yaml en utilisant `kubectl`.
                // Assurez-vous que le fichier deployment.yaml est présent à la racine du répertoire de travail.
                sh 'kubectl apply -f deployment.yaml'
            }
        }
    }
}
