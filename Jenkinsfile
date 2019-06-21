pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps { 
                sh 'clean' 
            }
        }
        stage('Test'){
            steps {
                sh 'make check'
                junit 'reports/**/*.xml' 
            }
        }
        stage('Deploy') {
            steps {
                sh 'deploy'
            }
        }
    }
}
