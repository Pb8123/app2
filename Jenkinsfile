@Library('shared-library@main') _

pipeline {

    agent any

    tools {
        maven 'maven399'
    }

    stages {

        stage('Build') {
            steps {
                mavenBuild()
            }
        }
        stage('Print') {
            steps {
                print()
            }
        }
        stage('Print1') {
            steps {
                print.benjicall()
            }
        }
    }

    post {

        success {
            script {
                emailNotification.successEmail()
            }
        }

        failure {
            script {
                emailNotification.failureEmail()
            }
        }

    }
}

