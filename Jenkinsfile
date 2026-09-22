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
                echo '=== Webhook Test 2 ==='
                sh 'echo "Execution Time: $(date)"'
                sh 'git log -1 --oneline'
            }
        }
    }
}
