pipeline {
    agent none
    environment { DOTNET_CLI_HOME="/tmp/dotnet_cli_home"}

    stages {
        stage('Build and Test dotnet') {
            agent { docker {image "mcr.microsoft.com/dotnet/sdk:6.0"}}
            steps {
                echo 'Building..'
                sh 'dotnet build'
                sh 'dotnet test'
            }
        }
        stage('Build and Test node') {
            agent { docker {image "node:17-bullseye"}}
            steps {
                echo 'Testing..'
                dir ("DotnetTemplate.Web"){
                   sh 'npm install && npm run build' 
                   sh 'npm t'
                   sh 'npm run lint'
                }
                
            }
        }
    }

}