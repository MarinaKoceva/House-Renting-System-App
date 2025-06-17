pipeline {
    agent any

    tools {
        msbuild 'MSBuild-v6' // това име трябва да съвпада с конфигурацията от Jenkins
    }

    stages {
        stage('Restore') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build') {
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Test') {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
