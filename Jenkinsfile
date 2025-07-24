first CODE_CHANGES = true
pipeline {
    agent any
    environment {
        BRANCH_NAME = env.BRANCH_NAME ?: '' // fallback if not set
    }
    stages {
        stage('Build') {
            when {
                expression {
                    return BRANCH_NAME == 'main' && CODE_CHANGES
                }
            }
            steps {
                echo 'Building the application...'
                // your build commands
            }
        }
        stage('Test') {
            when {
                expression {
                    return BRANCH_NAME != ''
                }
            }
            steps {
                echo 'Running tests...'
                // your test commands
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // your deploy commands
            }
        }
    }
}
