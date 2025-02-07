pipeline {
    agent any
    stages {
        stage('Test Slack') {
            steps {
                echo "About to send Slack notification..." // For debugging
                slackSend channel: '#jenkins-alerts', message: "Test notification from Jenkins!"
                echo "Slack notification sent (or attempted)..." // For debugging
            }
        }
    }
}
