pipeline {
    agent any
    environment {
	branchName = "feature"
    }

    stages {
        stage('checkout') {
           when {
              branchName 'feature'
	       }
           steps {
              echo"This is my first pipeline"
           }
    }
}
