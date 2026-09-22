pipeline {
    agent any

    triggers {
        // Пустое расписание: нет периодического опроса Git
        // GitHub Webhook настроим отдельно
        pollSCM('')
    }

    stages {
        stage('Validate Webhook Trigger') {
            steps {
                echo '=== Instant Webhook Event Received ==='
                sh 'echo "Execution Time: $(date)"'
                sh 'git log -1 --oneline'
            }
        }
    }
}
