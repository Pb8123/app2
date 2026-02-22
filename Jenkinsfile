@Library('shared-library@main') _

pipeline {

    agent any

    tools {
        maven 'maven399'
    }

    stages 
    {

        stage('Build') 
        {
            steps 
            {
                mavenBuild()
            }
        }
        stage('rajprintall') 
        {
            steps 
            {
                script
                {
                rajPrint()
                }
            }
        }
        
        stage('rajprintsingle') 
        {
            steps 
            {
                script
                {
                rajPrint.benjicall()
                }
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


