pipeline {
    agent { docker { image 'php' } }
    stages {
        stage('build') {
            environment {
            	THING = 'HI!';
            }
            steps {
                sh 'php --version'
                echo THING
            }
        }
    }
    post {
        always {
            echo 'One way or another, I have finished'
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
