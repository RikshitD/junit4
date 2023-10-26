pipeline {
    agent any
    tools {
        maven "m7"
    }
    stages {
        stage("Fetching") {
            steps {
                git branch: 'main', url: "https://github.com/RikshitD/junit4.git"
            }
        }
        stage("Compile") {
            steps {
                bat 'mvn compile'
            }
        }
        stage("Test") {
            steps {
                bat 'mvn test'
            }
        }
        stage("Package") {
            steps {
                bat 'mvn package'
            }
        }
        stage("Verify") {
            steps {
                bat 'mvn verify'
            }
        }
        stage("Install") {
            steps {
                bat 'mvn install'
            }
        }
    }
}
