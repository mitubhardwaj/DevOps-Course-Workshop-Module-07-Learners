pipeline {
    agent { docker {image "mcr.microsoft.com/dotnet/sdk:6.0"}}

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