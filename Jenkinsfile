pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Checkout source code
                checkout scm
                
                // Build Docker image
                sh 'docker build -t myfrontendapp .'
            }
        }
    }
}
