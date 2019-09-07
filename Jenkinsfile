pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                withEnv( ['MAVEN_HOME=D:/bin/apache-maven-3.6.1/bin'] ) {
                    bat 'mvn clean package'
                }
            }
            post {
                success {
                    echo '開始存檔...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}