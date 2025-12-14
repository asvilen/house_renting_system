pipeline {
    agent any

    stages {
        stage('Restore') {
            steps {
                echo 'Restoring...'
                dotnet restore
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                dotnet build --no-restore
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                dotnet test --no-build --verbosity normal
            }
        }
    }
}