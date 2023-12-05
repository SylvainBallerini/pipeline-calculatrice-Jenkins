pipeline {
    agent none
    environment {
        registryCredential = 'docker-hub-credential-id'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', registryCredential) {
                        def customImage = docker.build("my-custom-image")
                    }
                }
            }
        }
    }
}
