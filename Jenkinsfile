pipeline {
    agent any

    parameters {
        choice(name: "NODE_VERSION", choices: ["nodejsmlk"])
    }
    stages {
        stage('Build') {
            steps {

                nodejs(nodeJSInstallationName: "${params.NODE_VERSION}"){
                    sh "npm install"
                    sh "npm run build"
                    sh "npm test"
                }
            }
        }

    }
}