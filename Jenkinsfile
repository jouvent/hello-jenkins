pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        node {
            stage('build'){
                echo "building"
            }
        }
        stage('Deploy approval'){
            input "Deploy to prod?"
        }
        node {
            stage('deploy to prod'){
                echo "deploying"
            }
        }
    }
}
