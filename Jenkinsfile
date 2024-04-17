pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t mynodeapp .'
            }
        }
        stage('Deploy'){
            steps{
                sh 'docker save mynodeapp -o mynodeapp.tar'
                sh 'docker load -i mynodeapp.tar'
                sh 'docker run -d -p 3000:3000 mynodeapp'
            }
        }
    }
}
