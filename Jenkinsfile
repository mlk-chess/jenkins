pipeline {
    agent any

    tools {nodejs "nodejsmlk"}

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh "npm test"
            }
        }
    }
}