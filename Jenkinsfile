pipeline {
    agent any

    stages {
        stage('checkout') {
           when {
              branch 'master'
	       }
           steps {
              echo"This is my first pipeline"
           }
    }
}
