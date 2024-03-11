pipeline {
    agent any

    triggers {
        cron('H/10 * * 1') // Run every 10 minutes on Mondays
    }

    stages {
        stage('Build') {
            steps {
                script {
                    // Your build steps here
                    sh 'mvn clean install'
                }
            }
        }

        stage('Code Coverage') {
            steps {
                script {
                    // Generate code coverage report using Jacoco
                    sh 'mvn jacoco:report'
                }
            }
        }
    }
}
