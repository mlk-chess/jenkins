pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                nodejs(nodeJSInstallationName : 'Node 17.x')
                sh 'npm i -g pnpm'
                sh "pnpm install"
                sh "pnpm build"
                sh "pnpm test"
            }
        }
    }
}