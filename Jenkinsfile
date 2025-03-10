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
        stage("TEST parallel") {
            parallel{
            stage('Test shell - First') {
                steps {
                    echo "fist parallel step"
                }
            }
            stage('Test shell - Second') {
                steps {
                    echo "2nd parallel step"
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
