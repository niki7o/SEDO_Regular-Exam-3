pipeline {
    agent any

    stages {
        stage('Restore Dependencies') {
            steps {
                echo "Restoring NuGet packages..."
                bat 'dotnet restore'
            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
                bat 'dotnet build --configuration Release'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                bat 'dotnet test --configuration Release --verbosity normal'
            }
        }
    }

    
}