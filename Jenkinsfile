node {
    stage('build'){
        agent { docker { image 'maven:3.3.3' } }
        steps {
            sh 'mvn --version'
        }
    }
}
stage("Ready to deploy")
{
    input "Deploy to prod?"
}
node {
    stage('deploy to prod'){
        agent { docker { image 'veruscript/ebcli' } }
        steps {
            sh 'eb -h'
        }
    }
}
