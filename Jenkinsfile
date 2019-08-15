pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build'){
            echo "building"
        }
        stage('Deploy approval'){
            input "Deploy to prod?"
        }
        stage('deploy to prod'){
            echo "deploying"
        }
    }
}
