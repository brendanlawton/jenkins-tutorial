pipeline {
    agent { docker { image 'php' } }
    stages {
        stage('build') {
            environment {
            	THING = 'HI!';
            }
            steps {
                sh 'php --version'
                echo $THING
            }
        }
    }
}
