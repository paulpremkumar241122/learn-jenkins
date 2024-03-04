pipeline {

    agent { node { label 'workstation' } }
    options {
        ansiColor('xterm')
    }
    triggers { pollSCM('H/2 * * * *') }

    parameters {
        string(name: 'APP_INPUT', defaultValue: '', description: 'Just Input')
    }

    environment {
        SSH = credentials('SSH')
        DEMO_URL = "google.com"
    }

    stages {
        stage('Hello World - from pipeline SCM') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
                }
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


//