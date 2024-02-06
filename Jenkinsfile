pipeline {
    agent any
    tools {
        maven 'Maven-Jenkins'
    }
    stages {
        stage('Checkout stage') {
            steps {
                checkout scmGit(
                    branches: [[name: '*/main']],
                    extensions: [],
                    userRemoteConfigs: [[url: 'https://github.com/kunal7479/JenkinsSpringBoot.git']]
                )
            }
        }
        stage('Build Maven stage') {
            steps {
                bat 'mvn clean install'
            }
        }
    }
    post {
        success {
            echo 'Pipeline successfully executed!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
