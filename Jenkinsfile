pipeline {
    agent any

    tools {nodejs "nodejsmlk"}

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh "pnpm run build"
                sh "pnpm test"
            }
        }
    }
}