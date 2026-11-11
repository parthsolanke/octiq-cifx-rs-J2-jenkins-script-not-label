pipeline {
    agent any
    stages {
        stage('Verify') {
            steps {
                sh label: 'Run tests', script: 'cargo test'
                sh(returnStatus: true, label: 'Build', script: 'cargo build --all-targets')
            }
        }
    }
}
