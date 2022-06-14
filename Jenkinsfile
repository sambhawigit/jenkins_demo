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
              echo"This is my first pipeline"
           }
	}
    }
}
