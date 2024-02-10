pipeline {
    agent any
    environment {
        
        PATH = "/usr/local/bin:$PATH"
        KUBECONFIG = '/var/lib/jenkins/.kube/config'
    }
    stages {
        stage('Build') {
            steps {
                
                sh 'docker build -t app_flask .'
            }
        }
        
        stage('Deploy') {
            steps {
                
                sh 'kubectl apply -f deployment.yaml'
            }
        }
    }
}
