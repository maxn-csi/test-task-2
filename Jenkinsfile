pipeline{
    agent none
    stages {
        stage('Checkout SCM') {
            agent any
            steps{
                git credentialsId: 'Github', url: 'https://github.com/maxn-csi/test-task-2'
            }
        }
        stage('git pull') {
            when { changeset "code/*"}
            agent {
                node {
                    label 'task2'
                }
            } 
            steps{                
                sh "cd /home/project1 && sudo git pull"
            }            
        }
    }
}
