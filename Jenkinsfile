pipeline {
    agent any
    environment {
		branchName = "main"
    }

    stages {
        stage('checkout feature') {
			when {
                expression {
                    return env.branchName == "feature"
                }
            }
            steps {
              	echo "This is my first pipeline in feature branch"
				checkout([$class: 'GitSCM',
				branches: [[name: '*/feature']],
				extensions: [], 
				userRemoteConfigs: [[credentialsId: '0636c6bf-f984-4df3-a45f-7cdeaef53994',
				url: 'https://github.com/sambhawigit/jenkins_demo.git']]])
				sh 'python demo.py'
            }
	}
		stage('checkout main') {
			when {
                expression {
                    return env.branchName == "main"
                }
            }
            steps {
               	echo "This is my first pipeline in main branch"
				checkout([$class: 'GitSCM',
				branches: [[name: '*/main']],
				extensions: [], 
				userRemoteConfigs: [[credentialsId: '0636c6bf-f984-4df3-a45f-7cdeaef53994',
				url: 'https://github.com/sambhawigit/jenkins_demo.git']]])
				sh 'python demo.py'
            }
	}
	    
        stage("Run Tests") {
            steps {
                sh "echo SUCCESS on ${branchName}"
		        sh "echo ${UserName}"
            }
        }
   }
   
}
