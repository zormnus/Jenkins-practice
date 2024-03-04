pipeline {
    agent {
        docker {
            image 'gcc'
            args '-u root' 
        }
    }

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