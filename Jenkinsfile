pipeline {
    agent any
    tools {
        dotnetsdk 'MyNET10'  // Name you give in Global Tool Configuration
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