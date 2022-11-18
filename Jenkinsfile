pipeline {
    agent any
    stages("first stage") {
        stage("checkpout stage") {
            steps{
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'git-yomipounds', url: 'https://github.com/YomiPounds/job-repo.git']]])
            }  
        }
        stage("resource chk") {
            steps {
               sh "lscpu"
               echo "So easy to forget stuff"
            } 
        }
    }
}