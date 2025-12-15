pipeline {
    agent {
        docker { 
            image 'mcr.microsoft.com/dotnet/sdk:6.0'
        }
    }

    stages {
        stage('Restore') {
            steps {
                echo 'Restoring...'
                sh 'dotnet restore'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'dotnet build --no-restore'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}