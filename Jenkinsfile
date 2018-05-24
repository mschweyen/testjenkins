pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
                sh 'echo "Just another command 1"'
                sh 'echo "Just another command 2"'
                sh 'echo "Just another command 3"'
            }
        }
        
        stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }
        
        stage('Deploy - Production') {
            steps {
                sh 'echo "Deploy to production...."'
            }
        }

    }
}
