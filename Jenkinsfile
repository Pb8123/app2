@Library('shared-library@main')
@Library('shared-library1@main')
pipeline
{
    agent any
    tools 
    {
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
        stage('rajprint') 
        {
            steps 
            {
                script
                    {
                    rajPrint()
                    rajPrint.benjicall()
                    }        
            }
        }
    }
    post 
    {

        success 
        {
            script 
            {
                emailNotification.successEmail()
            }
        }

        failure 
        {
            script 
            {
                emailNotification.failureEmail()
            }
        }

    }
}

