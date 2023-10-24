pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Running build automation"
                sh "./gradlew build --no-daemon"
                archiveArtifacts artifacts: "dist/trainSchedule.zip", allowEmptyArchive: true
            }
        }
    }

    post {
        success {
            echo 'Build Successful!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}
