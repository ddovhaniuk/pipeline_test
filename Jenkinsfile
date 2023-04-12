pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
                sh 'echo "Building..."'
            }
            post
            {
                success
                {
                    echo "Archiving..."
                    archiveArtifacts:'**/target/*.war'
                }
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing..."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying..."'
            }
        }
    }
}
