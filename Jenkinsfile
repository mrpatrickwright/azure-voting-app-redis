pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo "$GIT_BRANCH"
                sh (script: 'echo Sup?')
            }
        }
        
        stage('Outy') {
            steps {
                echo 'We Out Here'
            }
        }
    }
}
