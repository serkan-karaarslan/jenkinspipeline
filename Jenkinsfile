pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                echo 'cleaning mvn package'
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}