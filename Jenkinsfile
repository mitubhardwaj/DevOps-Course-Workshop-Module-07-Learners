pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'dotnet build'

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
    }
}