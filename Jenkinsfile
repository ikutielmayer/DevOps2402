properties([pipelineTriggers([pollSCM('H * * * *')])])

pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Git Clone OK'
                git "https://github.com/ikutielmayer/DevOps2402.git"
            }
        }
        stage('Listado') {
            steps {
                sh "ls -l"
            }
        }
    }
}
