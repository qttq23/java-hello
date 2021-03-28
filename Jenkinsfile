pipeline {
    agent {
        docker { image 'gradle' }
    }

    stages 
    {
        stage('set up permission') {
            steps {
                sh "chmod +x gradlew"
            }
        }
        
    	stage('unit Test') {
            steps {
                sh "./gradlew test"
            }
        }

        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew run'
            }
        }
        stage('Deploy') {
            steps {
                sh 'gradle -version'
            }
        }
    }
}
