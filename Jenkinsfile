pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                echo"This is my first pipeline"
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '0636c6bf-f984-4df3-a45f-7cdeaef53994', url: 'https://github.com/sambhawigit/jenkins_demo.git']]])
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
    }
}
