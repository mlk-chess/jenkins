pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
            
                nodejs(nodeJSInstallationName: "nodejsmlk")
                sh "npm install"
                sh "npm run build"
                sh "npm test"
            }
        }
    }
}