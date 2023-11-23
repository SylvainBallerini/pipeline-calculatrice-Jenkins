pipeline {
    agent none

    stages {
        stage('Build') {
            steps {
                dockerImage = 'python:3.8-alpine3.16'
                sh 'python3.8 -m py_compile sources/prog.py sources/calc.py'
                stash(name: 'compiled-results', includes: 'sources/*.py*')
            }
        }
    }
}
