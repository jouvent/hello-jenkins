node {
    stage('build'){
        echo "building"
    }
}
stage("Ready to deploy")
{
    milestone
    input "Deploy to prod?"
}
node {
    stage('deploy to prod'){
        echo "deploying"
    }
}
