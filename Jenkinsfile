pipeline {
    agent any

    triggers {
        cron('H/2 * * * *')
        pollSCM('H/1 * * * *')
    }

    stages {

        stage('Clone Repository') {
            steps {
                echo "Cloning Repository..."
            }
        }

        stage('Build') {
            steps {
                echo "Building Project..."
            }
        }

        stage('Echo Build Status') {
            steps {
                echo "Build Successful!"
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '**/*'
            }
        }
    }
}

