pipeline {
    agent any

    parameters {
        choice(name: "NODE_VERSION", choices: ["nodejs", "nodejsmlk"])
    }
    stages {
        stage('Build') {
            steps {

                nodejs(nodeJSInstallationName: "${params.NODE_VERSION}"){
                    sh "node -v"
                    sh "npm install"
                    sh "npm run build"
                    sh "npm test"
                }
            }
        }
    }
}