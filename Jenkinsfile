
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Git Checkout Branch') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], browser: github('https://github.com/faseeh-22/25'), extensions: [cloneOption(honorRefspec: true, noTags: true, reference: '', shallow: false), localBranch('master'),  [$class: 'RelativeTargetDirectory', relativeTargetDir: 'git-checkout-pipeline']], userRemoteConfigs: [[credentialsId: 'git-checkout-pipeline', url: 'https://github.com/faseeh-22/25']])
            }
        }
    }
}
