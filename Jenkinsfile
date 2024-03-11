pipeline {
    agent any
    tools {
            maven 'maven3'
            jdk 'JDK'
    }
    triggers {
        cron('H/10 * * * 1') // Run every 10 minutes on Mondays
    }

    stages {
        stage('Build') {
            steps {
                script {
                    // Your build steps here
                    bat 'mvn clean install'
                }
            }
        }

        stage('Code Coverage') {
            steps {
                script {
                    // Generate code coverage report using Jacoco
                    bat 'mvn jacoco:report'
                }
            }
        }
    }
}
