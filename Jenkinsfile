pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/1.0.0']], userRemoteConfigs: [[url: 'https://github.com/bigorado/vector.git']]])
            }
        }
        stage('Molecule Test') {
            steps {
                sh 'molecule test'
            }
        }
    }
}
