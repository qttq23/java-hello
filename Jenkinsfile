pipeline {
    agent {
        docker { image 'gradle' }
    }

    stages 
    {
    	stage('unit Test') {
            steps {
                sh "gradlew test"
            }
        }

        stage('Build') {
            steps {
                sh 'gradlew build'
            }
        }
        stage('Test') {
            steps {
                sh 'gradlew run'
            }
        }
        stage('Deploy') {
            steps {
                sh 'gradle -version'
            }
        }
    }
}
