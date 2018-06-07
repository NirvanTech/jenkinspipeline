pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
               // checkout scm
                withAnt(installation: 'Ant1.10.3') {
                    bat "ant clean"
                }
                /*script {
                    def antVersion = 'Ant1.10.3'
                    withEnv( ["ANT_HOME=${tool antVersion}"] ) {
                        bat '"%ANT_HOME%"\\bin\\ant.bat clean'
                    }
                }*/
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
