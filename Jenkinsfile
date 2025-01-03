pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: ' https://github.com/Kobby-Jones/Static_Website-Deployment_with_Jenkins.git'
            }
        }
        stage('Deploy to S3') {
            steps {
                sh 'aws s3 sync . s3://jenkins-static-website --delete'
            }
        }
    }
}
