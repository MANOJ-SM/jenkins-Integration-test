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
        jiraAddComment site: 'MyJiraCloud', idOrKey: 'JIRA-123', comment: "Build & Deployment Successful"  // Replace MyJira with your site name
    }
    failure {
        jiraAddComment site: 'MyJiraCloud', idOrKey: 'JIRA-123', comment: "Build Failed"  // Replace MyJira with your site name
    }
}
    }
}
