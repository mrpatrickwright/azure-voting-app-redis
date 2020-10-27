pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
                sh (script: 'echo Sup?')
                sh (script: 'sudo usermod -a -G docker jenkins')
            }
        }
        stage('Docker Build'){
            steps{
                sh(script: 'docker images -a')
                sh(script:'''
                    cd azure-vote/
                    docker build -t jenkins-pipeline .
                    docker images -a
                    cd ..
                
                
                ''')
            }
        }
        stage('Outy') {
            steps {
                echo 'We Out Here'
            }
        }
    }
}
