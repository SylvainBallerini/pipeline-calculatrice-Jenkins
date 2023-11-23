pipeline {
    agent {
        label 'docker'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('python:3.8-alpine3.16').inside {
                        sh 'python3.8 -m py_compile sources/prog.py sources/calc.py'
                        stash(name: 'compiled-results', includes: 'sources/*.py*')
                    }
                }
            }
        }
    }
}
