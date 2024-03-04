pipeline {

    agent { node { label 'workstation' } }

    environment {
        SSH = credentials('SSH')
        DEMO_URL = "google.com"
    }

    stages {
        stage('Hello World - from pipeline SCM') {
            steps {
                echo 'Hello World - from pipeline SCM'
                sh 'env'
                sh 'DEMO_URL'
            }
        }
    }

    post {
        always {
            sh 'echo post'
        }
    }
}
