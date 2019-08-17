pipeline {
    agent none
    stages {
        stage('build'){
            agent { docker { image 'maven:3.3.3' } }
            steps {
                sh 'mvn --version'
            }
        }
        stage("Ready to deploy") {
            steps {
                milestone()
                input "Deploy to staging?"
            }
        }
        stage('deploy to staging') {
            agent { docker { image 'veruscript/ebcli' } }
            steps {
                sh 'eb -h'
            }
        }
        stage("Ready to deploy") {
            steps {
                milestone()
                input "Deploy to prod?"
            }
        }
        stage('deploy to prod') {
            agent { docker { image 'veruscript/ebcli' } }
            steps {
                sh 'eb -h'
            }
        }
    }
}
