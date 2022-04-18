pipeline {
    agent any
    stages {
        stage('hello'){
            steps {
                sh(script 'docker images -a')
                sh(script: """
                    cd docker/
                    docker images -a
                    docker build -t example .
                    docker images -a
                    cd ..
                """)
            }
        }
    }
}