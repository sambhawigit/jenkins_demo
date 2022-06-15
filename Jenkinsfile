pipeline {
    agent any
    environment {
	branchName = "feature"
    }

    stages {
        stage('checkout') {
           when {
              branch 'feature'
	   }
           steps {
              echo "This is my first pipeline in feature branch"
	      checkout([$class: 'GitSCM',
			branches: [[name: '*/feature']],
			extensions: [], 
			userRemoteConfigs: [[credentialsId: '0636c6bf-f984-4df3-a45f-7cdeaef53994',
			url: 'https://github.com/sambhawigit/jenkins_demo.git']]])
           }
	}
	stage('checkout') {
           when {
              branch 'main'
	   }
           steps {
              echo "This is my first pipeline in main branch"
	      checkout([$class: 'GitSCM',
			branches: [[name: '*/main']],
			extensions: [], 
			userRemoteConfigs: [[credentialsId: '0636c6bf-f984-4df3-a45f-7cdeaef53994',
			url: 'https://github.com/sambhawigit/jenkins_demo.git']]])
           }
	}
	    
        stage("Run Tests") {
            steps {
                sh "echo SUCCESS on ${branchName}"
        }
        }
   }
   
}
