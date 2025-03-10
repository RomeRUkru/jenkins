pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Print pwd') {
            steps {
                sh '''
                    pwd
                    ls -la
                    echo "my lil pony is here <3"
                '''
            }
        }
        stage("TEST PARALLEL") {
            parallel{
            stage('Test shell - First') {
                steps {
                    sh "ls -la"
                }
            }
            stage('Test shell - Second') {
                steps {
                    sh "pwd"
                }
            }
            }
        }
    stage('Bye, Bye') {
        steps {
            echo 'Bye World'
        }
    }
    }
}
