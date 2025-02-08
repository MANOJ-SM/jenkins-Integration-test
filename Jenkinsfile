pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
    post {
        success {
            jiraAddComment idOrKey: 'SCRUM-1', comment: "Build & Deployment Successful "
        }
        failure {
            jiraAddComment idOrKey: 'SCRUM-1', comment: "Build Failed "
        }
    }
}
