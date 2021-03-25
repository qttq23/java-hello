pipeline {
    agent any

    stages 
    {
    	stage('unit Test') {
            steps {
                bat "gradlew test"
            }
        }

        stage('Build') {
            steps {
                bat 'gradlew build'
            }
        }
        stage('Test') {
            steps {
                bat 'gradlew run'
            }
        }
        stage('Deploy') {
            steps {
                bat 'Xcopy /I /E ".\\app\\build\\distributions"  "D:\\multi\\output" '
            }
        }
    }
}