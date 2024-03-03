pipeline {

    agent { node { label 'workstation' } }

    environment {
        SSH = credentials('SSH')
    }

    stages {
        stage('Hello World - from pipeline SCM') {
            steps {
                echo 'Hello World - from pipeline SCM'
                sh 'env'
            }
        }
    }

    post {
        always {
            sh 'echo post'
        }
    }
}
