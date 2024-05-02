pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    docker.build('my-react-app', '-f Dockerfile .')
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    docker.image('my-react-app').push()
                }
            }
        }
    }
}
