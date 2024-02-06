pipeline{
    agent any
    tools{
        maven 'Jenkin-maven'
    }
    stages {
        stage ('Checkout')
        {
            steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/kunal7479/JenkinsSpringBoot.git']])
            }
        }
        stage ('Build Maven'){
            steps
            {
                bat 'mvn clean install' 
            }
        }
    }
}
