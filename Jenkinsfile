pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                checkout scm
                script {
                    def antVersion = 'Ant1.10.3'
                    withEnv( ["ANT_HOME=${tool antVersion}"] ) {
                        bat '"%ANT_HOME%"\\bin\\ant.bat clean'
                    }
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
