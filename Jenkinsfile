pipeline{
    agent any
    stages {
        stage('Checkout SCM') {
            steps{
                git credentialsId: 'Github', url: 'https://github.com/maxn-csi/test-task-2'
            }
        }
        stage('git pull') {
            when { changeset "code/*"}
            steps{
                sshagent(credentials : ['task2_ssh']) {
                    sh 'ssh -o StrictHostKeyChecking=no \
                    -oKexAlgorithms=+diffie-hellman-group1-sha1 \
                    ubuntu@52.205.4.99 "cd /home/project1 ; sudo git pull"'
                }
            }            
        }
    }
}
