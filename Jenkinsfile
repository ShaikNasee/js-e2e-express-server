pipeline {
    agent { label 'jdk11-mvn-3.8.5' }
    stages { 
        stage('SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/ShaikNasee/js-e2e-express-server.git'
            }
        }
        stage('installing npm') {
            steps {
                sh 'npm install'
            }
        }
        stage('test') {
            steps {
                sh 'npm test'
            }
        }
        stage('build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}