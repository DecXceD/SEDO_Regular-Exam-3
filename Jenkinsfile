pipeline {
    agent any

    triggers {
            pollSCM('H/5 * * * *')
    }
    stages {
        stage("Build .NET Project") {
            steps {
                bat 'dotnet build'
            }
        }
        stage("Run Unit and Integration Tests") {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}