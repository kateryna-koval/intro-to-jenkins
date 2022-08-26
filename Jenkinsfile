pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
    post {
        always {
            mail to: 'kateryna.koval@ringteam.com',
                 subject: "Pipeline: ${currentBuild.fullDisplayName}",
                 body: "Build URL ${env.BUILD_URL}"
        }
    }
}

