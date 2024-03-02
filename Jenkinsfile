pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o fibapp app.cpp'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'fibapp', fingerprint: true
            }
        }
    }
}