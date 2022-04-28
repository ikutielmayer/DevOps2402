properties([parameters([string(defaultValue: 'Yekutiel', description: 'WHAT IS YOUR nAME?', name: 'NAME')]), pipelineTriggers([pollSCM('H * * * *')])])

pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Git Clone OK'
                echo NAME
                git "https://github.com/ikutielmayer/DevOps2402.git"
            }
        }
        stage('Listado') {
            steps {
                sh "ls -l"
            }
        }
          stage('Ejecucion') {
            steps {
                python3 main.py
            }
        }
    }
}
