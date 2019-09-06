pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'set MAVEN_HOME=D:\bin\apache-maven-3.6.1'
                bat 'set PATH=%MAVEN_HOME%\bin;%PATH%'
                bat 'mvn clean package'
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